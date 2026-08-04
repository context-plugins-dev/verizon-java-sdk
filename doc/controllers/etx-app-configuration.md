# ETX App Configuration

Manage geofence-based application configurations.

```java
ETXAppConfigurationController eTXAppConfigurationController = client.getETXAppConfigurationController();
```

## Class Name

`ETXAppConfigurationController`

## Methods

* [Get Configuration List](../../doc/controllers/etx-app-configuration.md#get-configuration-list)
* [Get Configuration](../../doc/controllers/etx-app-configuration.md#get-configuration)
* [Create Configuration](../../doc/controllers/etx-app-configuration.md#create-configuration)
* [Update Configuration](../../doc/controllers/etx-app-configuration.md#update-configuration)
* [Delete Configuration](../../doc/controllers/etx-app-configuration.md#delete-configuration)


# Get Configuration List

This endpoint fetches and returns the list of configurations defined by the Vendor. The list contains the configurations' identifier, name, description, and active flag. The vendor ID is provided when the configuration is created through the POST request.

Note: The user needs to authenticate with their ThingSpace credentials using the Access/Bearer and Session/M2M tokens in order to call this API.

```java
CompletableFuture<ApiResponse<List<ConfigurationListItem>>> getConfigurationListAsync(
    final String vendorID)
```

## Authentication

This endpoint requires [thingspace_oauth](../../doc/auth/oauth-2-client-credentials-grant.md) **AND** [sessionToken](../../doc/auth/custom-header-signature-1.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vendorID` | `String` | Header, Required | The vendor's identifier<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `64`, *Pattern*: `^[a-zA-Z0-9]+$` |

## Server

`Server.IMP_SERVER`

## Response Type

**200**: Configuration list was queried successfully

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`List<ConfigurationListItem>`](../../doc/models/configuration-list-item.md).

## Example Usage

```java
String vendorID = "VerizonETX";

eTXAppConfigurationController.getConfigurationListAsync(vendorID).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof ResponseErrorException) {
        ResponseErrorException responseErrorException = (ResponseErrorException) cause;
        responseErrorException.printStackTrace();
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
| 403 | Forbidden | [`ResponseErrorException`](../../doc/models/response-error-exception.md) |
| 404 | Configuration not found | [`ResponseErrorException`](../../doc/models/response-error-exception.md) |
| 429 | Too many requests | [`ResponseErrorException`](../../doc/models/response-error-exception.md) |
| Default | unexpected error | [`ResponseErrorException`](../../doc/models/response-error-exception.md) |


# Get Configuration

This endpoint fetches and returns a specific configuration's details. The configuration ID parameter, which was provided when the configuration was created through the POST request, is need to retrieve the configuration details.

Note: The user needs to authenticate with their ThingSpace credentials using the Access/Bearer and Session/M2M tokens in order to call this API.

```java
CompletableFuture<ApiResponse<GeoFenceConfigurationResponse>> getConfigurationAsync(
    final String id,
    final String vendorID)
```

## Authentication

This endpoint requires [thingspace_oauth](../../doc/auth/oauth-2-client-credentials-grant.md) **AND** [sessionToken](../../doc/auth/custom-header-signature-1.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Query, Required | The configuration identifier<br><br>**Constraints**: *Minimum Length*: `32`, *Maximum Length*: `36`, *Pattern*: `^[0-9a-fA-F]{8}-?[0-9a-fA-F]{4}-?4[0-9a-fA-F]{3}-?[89abAB][0-9a-fA-F]{3}-?[0-9a-fA-F]{12}$` |
| `vendorID` | `String` | Header, Required | The vendor's identifier<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `64`, *Pattern*: `^[a-zA-Z0-9]+$` |

## Server

`Server.IMP_SERVER`

## Response Type

**200**: Configuration found

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`GeoFenceConfigurationResponse`](../../doc/models/geo-fence-configuration-response.md).

## Example Usage

```java
String id = "18bac1ff-c7bd-44d9-a7ad-06a093a94713";
String vendorID = "VerizonETX";

eTXAppConfigurationController.getConfigurationAsync(id, vendorID).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof ResponseErrorException) {
        ResponseErrorException responseErrorException = (ResponseErrorException) cause;
        responseErrorException.printStackTrace();
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
| 403 | Forbidden | [`ResponseErrorException`](../../doc/models/response-error-exception.md) |
| 404 | Configuration not found | [`ResponseErrorException`](../../doc/models/response-error-exception.md) |
| 429 | Too many requests | [`ResponseErrorException`](../../doc/models/response-error-exception.md) |
| Default | unexpected error | [`ResponseErrorException`](../../doc/models/response-error-exception.md) |


# Create Configuration

This endpoint creates a new configuration in the system. The data for the new configuration should be provided as JSON in the body of the POST request. The system will return with a unique ID for the configuration, which is needed for any further manipulation (update or delete) of the configuration.

Note: The user needs to authenticate with their ThingSpace credentials using the Access/Bearer and Session/M2M tokens in order to call this API.

```java
CompletableFuture<ApiResponse<GeoFenceConfigurationResponse>> createConfigurationAsync(
    final String vendorID,
    final GeoFenceConfigurationRequest body)
```

## Authentication

This endpoint requires [thingspace_oauth](../../doc/auth/oauth-2-client-credentials-grant.md) **AND** [sessionToken](../../doc/auth/custom-header-signature-1.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vendorID` | `String` | Header, Required | The vendor's identifier<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `64`, *Pattern*: `^[a-zA-Z0-9]+$` |
| `body` | [`GeoFenceConfigurationRequest`](../../doc/models/geo-fence-configuration-request.md) | Body, Required | - |

## Server

`Server.IMP_SERVER`

## Response Type

**201**: Configuration created

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`GeoFenceConfigurationResponse`](../../doc/models/geo-fence-configuration-response.md).

## Example Usage

```java
String vendorID = "VerizonETX";
GeoFenceConfigurationRequest body = new GeoFenceConfigurationRequest.Builder(
    new GeoFence.Builder(
        TypeEnum.FEATURECOLLECTION,
        Arrays.asList(
            new FeatureItem.Builder(
                Type1Enum.FEATURE,
                Geometry.fromLineString(
                    new LineString.Builder(
                        Type2Enum.LINESTRING,
                        Arrays.asList(
                            Arrays.asList(
                                51.53D,
                                51.54D
                            ),
                            Arrays.asList(
                                51.53D,
                                51.54D
                            )
                        )
                    )
                    .build()
                ),
                ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}")
            )
            .build()
        )
    )
    .build(),
    Arrays.asList(
        Message4.fromMessage(
            new Message.Builder(
                false,
                Arrays.asList(
                    RoadUserTypesEnum.VULNERABLEROADUSER
                ),
                Arrays.asList(
                    TriggerConditionEnum.CROSSING
                ),
                new GenericPayload.Builder(
                    "messageType4",
                    "messageFormat6",
                    "payload0"
                )
                .build()
            )
            .build()
        )
    ),
    false
)
.messageStandard(MessageStandardEnum.SAE)
.build();

eTXAppConfigurationController.createConfigurationAsync(vendorID, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof ResponseErrorException) {
        ResponseErrorException responseErrorException = (ResponseErrorException) cause;
        responseErrorException.printStackTrace();
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
| 400 | Invalid configuration | [`ResponseErrorException`](../../doc/models/response-error-exception.md) |
| 403 | Forbidden | [`ResponseErrorException`](../../doc/models/response-error-exception.md) |
| 429 | Too many requests | [`ResponseErrorException`](../../doc/models/response-error-exception.md) |
| Default | unexpected error | [`ResponseErrorException`](../../doc/models/response-error-exception.md) |


# Update Configuration

This endpoint updates an existing configuration. Similar to POST, the updated data for the configuration should be provided as JSON in the body of the PUT request. The configuration ID parameter, which was provided by the POST (create) operation, is required to do any updates on the configuration.

Note: The user needs to authenticate with their ThingSpace credentials using the Access/Bearer and Session/M2M tokens in order to call this API.

```java
CompletableFuture<ApiResponse<Void>> updateConfigurationAsync(
    final String vendorID,
    final String id,
    final GeoFenceConfigurationUpdateRequest body)
```

## Authentication

This endpoint requires [thingspace_oauth](../../doc/auth/oauth-2-client-credentials-grant.md) **AND** [sessionToken](../../doc/auth/custom-header-signature-1.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vendorID` | `String` | Header, Required | The vendor's identifier<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `64`, *Pattern*: `^[a-zA-Z0-9]+$` |
| `id` | `String` | Query, Required | The configuration identifier<br><br>**Constraints**: *Minimum Length*: `32`, *Maximum Length*: `36`, *Pattern*: `^[0-9a-fA-F]{8}-?[0-9a-fA-F]{4}-?4[0-9a-fA-F]{3}-?[89abAB][0-9a-fA-F]{3}-?[0-9a-fA-F]{12}$` |
| `body` | [`GeoFenceConfigurationUpdateRequest`](../../doc/models/geo-fence-configuration-update-request.md) | Body, Required | - |

## Server

`Server.IMP_SERVER`

## Response Type

**204**: Configuration applied

`void`

## Example Usage

```java
String vendorID = "VerizonETX";
String id = "18bac1ff-c7bd-44d9-a7ad-06a093a94713";
GeoFenceConfigurationUpdateRequest body = new GeoFenceConfigurationUpdateRequest.Builder()
    .messageStandard(MessageStandardEnum.SAE)
    .build();

eTXAppConfigurationController.updateConfigurationAsync(vendorID, id, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof ResponseErrorException) {
        ResponseErrorException responseErrorException = (ResponseErrorException) cause;
        responseErrorException.printStackTrace();
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
| 400 | Invalid configuration | [`ResponseErrorException`](../../doc/models/response-error-exception.md) |
| 403 | Forbidden | [`ResponseErrorException`](../../doc/models/response-error-exception.md) |
| 404 | Configuration not found | [`ResponseErrorException`](../../doc/models/response-error-exception.md) |
| 429 | Too many requests | [`ResponseErrorException`](../../doc/models/response-error-exception.md) |
| Default | unexpected error | [`ResponseErrorException`](../../doc/models/response-error-exception.md) |


# Delete Configuration

This endpoint deletes a specific configuration from the system. It requires the configuration ID parameter, which was provided by the POST (create) operation.

Note: The user needs to authenticate with their ThingSpace credentials using the Access/Bearer and Session/M2M tokens in order to call this API.

```java
CompletableFuture<ApiResponse<Void>> deleteConfigurationAsync(
    final String vendorID,
    final String id)
```

## Authentication

This endpoint requires [thingspace_oauth](../../doc/auth/oauth-2-client-credentials-grant.md) **AND** [sessionToken](../../doc/auth/custom-header-signature-1.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vendorID` | `String` | Header, Required | The vendor's identifier<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `64`, *Pattern*: `^[a-zA-Z0-9]+$` |
| `id` | `String` | Query, Required | The configuration identifier<br><br>**Constraints**: *Minimum Length*: `32`, *Maximum Length*: `36`, *Pattern*: `^[0-9a-fA-F]{8}-?[0-9a-fA-F]{4}-?4[0-9a-fA-F]{3}-?[89abAB][0-9a-fA-F]{3}-?[0-9a-fA-F]{12}$` |

## Server

`Server.IMP_SERVER`

## Response Type

**204**: Configuration deleted

`void`

## Example Usage

```java
String vendorID = "VerizonETX";
String id = "18bac1ff-c7bd-44d9-a7ad-06a093a94713";

eTXAppConfigurationController.deleteConfigurationAsync(vendorID, id).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof ResponseErrorException) {
        ResponseErrorException responseErrorException = (ResponseErrorException) cause;
        responseErrorException.printStackTrace();
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
| 403 | Forbidden | [`ResponseErrorException`](../../doc/models/response-error-exception.md) |
| 429 | Too many requests | [`ResponseErrorException`](../../doc/models/response-error-exception.md) |
| Default | unexpected error | [`ResponseErrorException`](../../doc/models/response-error-exception.md) |

