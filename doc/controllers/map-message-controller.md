# Map-Message-Controller

Endpoints for ingesting, querying, and deleting V2X MAP messages.

```java
MapMessageController mapMessageController = client.getMapMessageController();
```

## Class Name

`MapMessageController`

## Methods

* [Download MAP Messages](../../doc/controllers/map-message-controller.md#download-map-messages)
* [Ingest MAP Messages](../../doc/controllers/map-message-controller.md#ingest-map-messages)
* [Query Map Messages](../../doc/controllers/map-message-controller.md#query-map-messages)
* [Delete Map Message](../../doc/controllers/map-message-controller.md#delete-map-message)


# Download MAP Messages

**This endpoint is deprecated.**

This endpoint is deprecated. (Use /api/v2/mapdata/query for new integrations).

This endpoint allows user to download SAE J2735 or ETSI MAP messages in ASN.1 UPER base64 encoded format. The area for the MAP messages is needed to be defined in the query.

**Required request header:** `Accept` — specifies the response format. Omitting this header will result in a `400 Bad Request`. Supported values:

- `text/plain` — ASN.1 UPER base64-encoded MAP messages (one per line)
- `application/json` — JSON-encoded MAP messages

```java
CompletableFuture<ApiResponse<String>> downloadMAPMessagesAsync(
    final String vendorID,
    final GeofencePolygon geofence)
```

## Authentication

This endpoint requires [thingspace_oauth](../../doc/auth/oauth-2-client-credentials-grant.md) **AND** [sessionToken](../../doc/auth/custom-header-signature-1.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vendorID` | `String` | Header, Required | The VendorID set during the Vendor registration call.<br><br>**Constraints**: *Maximum Length*: `64`, *Pattern*: `^[a-zA-Z0-9]+$` |
| `geofence` | [`GeofencePolygon`](../../doc/models/geofence-polygon.md) | Query, Required | GeoJSON Polygon defining the area to retrieve MAP messages for. |

## Server

`Server.IMP_SERVER`

## Response Type

**200**: Line separated ASN.1 UPER J2735/ETSI base64 encoded MapData messages

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type `String`.

## Example Usage

```java
String vendorID = "VzMapManager";
GeofencePolygon geofence = new GeofencePolygon.Builder()
    .type(ETXMAPMessageGeofenceGeometryEnum.POLYGON)
    .coordinates(Arrays.asList(
        Arrays.asList(
            -77.479395D,
            38.990773D
        ),
        Arrays.asList(
            -77.114566D,
            38.99944D
        ),
        Arrays.asList(
            -77.100228D,
            38.817204D
        ),
        Arrays.asList(
            -77.418059D,
            38.827754D
        ),
        Arrays.asList(
            -77.479395D,
            38.990773D
        )
    ))
    .build();

mapMessageController.downloadMAPMessagesAsync(vendorID, geofence).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof MdmErrorResponseException) {
        MdmErrorResponseException mdmErrorResponseException = (MdmErrorResponseException) cause;
        mdmErrorResponseException.printStackTrace();
    } else {
        // fallback for unexpected errors
        exception.printStackTrace();
    }

    return null;
});
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Request | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |
| 401 | Unauthorized | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |
| 403 | Forbidden | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |
| 404 | Not found | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |
| 429 | Too many requests | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |
| 503 | Internal server error | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |
| Default | unexpected error | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |


# Ingest MAP Messages

This endpoint allows the user to upload map messages in ASN.1 UPER base64 encoded format or JER (JSON) formats. The MAP data message can have more than one intersections in it.
Both SAE and ETSI defined MAP messages are supported. The SAE type MAP messages have to be wrapped in a MessageFrame, as defined in the SAE J2735 standard.
The ETSI type MAP messages are expected as MAPEM structures that include the ETSI header, as defined in the ETSI TS 103 301 standard.
Note: The user needs to authenticate with their ThingSpace credentials using the Access/Bearer and Session/M2M tokens in order to call this API.

**Required request header:** `Content-Type` — specifies the format of the request body. Omitting or sending an unsupported value will result in a `415 Unsupported Media Type`. Supported values:

- `text/plain` — ASN.1 UPER base64-encoded MAP message
- `application/json` — JSON representation of the MAP message

```java
CompletableFuture<ApiResponse<String>> ingestMAPMessagesAsync(
    final String vendorID,
    final ETXMessageStandardEnum mapDataMessageStandard,
    final ETXMAPDataIngestRequest body)
```

## Authentication

This endpoint requires [thingspace_oauth](../../doc/auth/oauth-2-client-credentials-grant.md) **AND** [sessionToken](../../doc/auth/custom-header-signature-1.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vendorID` | `String` | Header, Required | The VendorID set during the Vendor registration call.<br><br>**Constraints**: *Maximum Length*: `64`, *Pattern*: `^[a-zA-Z0-9]+$` |
| `mapDataMessageStandard` | [`ETXMessageStandardEnum`](../../doc/models/etx-message-standard-enum.md) | Header, Required | Select which V2X messaging standard will be used for the message generation. The following options are supported:<br><br>- "etsi": The message will be generated using the ETSI (European) standard (e.g. MAPEM).<br>- "sae": The message will be generated using the SAE J2735 (North American) standard (e.g. MAP).<br>- if not sent while POST, defaults to "sae"<br><br>**Constraints**: *Maximum Length*: `4`, *Pattern*: `^(etsi\|sae)$` |
| `body` | [`ETXMAPDataIngestRequest`](../../doc/models/etxmap-data-ingest-request.md) | Body, Required | UPER/ASN.1 J2735/ETSI base64 encoded MapData message or JSON representation of the MapData message. |

## Server

`Server.IMP_SERVER`

## Response Type

**201**: Map message/s successfully uploaded

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type `String`.

## Example Usage

```java
String vendorID = "VzMapManager";
ETXMessageStandardEnum mapDataMessageStandard = ETXMessageStandardEnum.SAE;
ETXMAPDataIngestRequest body = new ETXMAPDataIngestRequest.Builder(
    18,
    ApiHelper.deserialize("{\"intersections\":[{\"id\":{\"region\":0,\"id\":156},\"laneWidth\":366,\"refPoint\":{\"lat\":389284111,\"long\":-772410713},\"revision\":3}],\"msgIssueRevision\":3}")
)
.build();

mapMessageController.ingestMAPMessagesAsync(vendorID, mapDataMessageStandard, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof MdmErrorResponseException) {
        MdmErrorResponseException mdmErrorResponseException = (MdmErrorResponseException) cause;
        mdmErrorResponseException.printStackTrace();
    } else {
        // fallback for unexpected errors
        exception.printStackTrace();
    }

    return null;
});
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Request | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |
| 401 | Unauthorized | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |
| 403 | Forbidden | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |
| 405 | Method not allowed | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |
| 429 | Too many requests | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |
| 503 | Internal server error | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |
| Default | unexpected error | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |


# Query Map Messages

This endpoint allows users to download SAE J2735 or ETSI MAP messages as a JSON list.
Depending on the expectedType parameter, the response contains either ASN.1 UPER base64-encoded messages with their respective region and intersection IDs, or fully decoded JSON messages.
The area for MAP message retrieval must be defined in the request body using one of two methods:
An array of region and intersection ID pairs, or a GeoJSON geofence specification.

```java
CompletableFuture<ApiResponse<List<Object>>> queryMapMessagesAsync(
    final String vendorID,
    final MapDataQueryRequest body)
```

## Authentication

This endpoint requires [thingspace_oauth](../../doc/auth/oauth-2-client-credentials-grant.md) **AND** [sessionToken](../../doc/auth/custom-header-signature-1.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vendorID` | `String` | Header, Required | The VendorID set during the Vendor registration call.<br><br>**Constraints**: *Maximum Length*: `64`, *Pattern*: `^[a-zA-Z0-9]+$` |
| `body` | [`MapDataQueryRequest`](../../doc/models/containers/map-data-query-request.md) | Body, Required | Request structure for querying MAP records. Provide either regionIntersectionPairs (coordinates) or geoJson, not both. |

## Server

`Server.IMP_SERVER`

## Response Type

**200**: Successfully retrieved MAP messages. Returns a JSON array where each element contains either a base64 string or parsed message object.

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type `List<Object>`.

## Example Usage

```java
String vendorID = "VzMapManager";
MapDataQueryRequest body = MapDataQueryRequest.fromETXMAPMessageIntersectionCoordinates(
    new ETXMAPMessageIntersectionCoordinates.Builder(
        Arrays.asList(
            new RegionIntersectionPair.Builder(
                5233
            )
            .regionId(100)
            .build()
        )
    )
    .messageStandard(ETXMessageStandardEnum.SAE)
    .expectedType(ETXExpectedTypeEnum.BASE64)
    .pageSize(50)
    .build()
);

mapMessageController.queryMapMessagesAsync(vendorID, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof MdmErrorResponseException) {
        MdmErrorResponseException mdmErrorResponseException = (MdmErrorResponseException) cause;
        mdmErrorResponseException.printStackTrace();
    } else {
        // fallback for unexpected errors
        exception.printStackTrace();
    }

    return null;
});
```

## Example Response

```
[
  {
    "messageStandard": "sae",
    "regionId": 100,
    "intersectionId": 5233,
    "payload": "asdfKDSiORel23=="
  }
]
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Request | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |
| 401 | Unauthorized | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |
| 403 | Forbidden | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |
| 405 | Method not allowed | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |
| 429 | Too many requests | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |
| 503 | Internal server error | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |
| Default | unexpected error | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |


# Delete Map Message

Removes a map message for the specified region and intersection ID.

```java
CompletableFuture<ApiResponse<Void>> deleteMapMessageAsync(
    final String regionId,
    final String i10nid)
```

## Authentication

This endpoint requires [thingspace_oauth](../../doc/auth/oauth-2-client-credentials-grant.md) **AND** [sessionToken](../../doc/auth/custom-header-signature-1.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `regionId` | `String` | Template, Required | Region ID to filter the map messages. |
| `i10nid` | `String` | Template, Required | Intersection ID to filter the map messages. |

## Server

`Server.IMP_SERVER`

## Response Type

**204**: Deleted successfully (No Content)

`void`

## Example Usage

```java
String regionId = "0";
String i10nid = "58399";

mapMessageController.deleteMapMessageAsync(regionId, i10nid).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof MdmErrorResponseException) {
        MdmErrorResponseException mdmErrorResponseException = (MdmErrorResponseException) cause;
        mdmErrorResponseException.printStackTrace();
    } else {
        // fallback for unexpected errors
        exception.printStackTrace();
    }

    return null;
});
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Request | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |
| 401 | Unauthorized | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |
| 403 | Forbidden | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |
| 404 | Not found | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |
| 429 | Too many requests | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |
| 503 | Internal server error | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |
| Default | unexpected error | [`MdmErrorResponseException`](../../doc/models/mdm-error-response-exception.md) |

