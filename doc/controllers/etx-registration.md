# ETX Registration

Manage device registration and connection.

```java
ETXRegistrationController eTXRegistrationController = client.getETXRegistrationController();
```

## Class Name

`ETXRegistrationController`

## Methods

* [Register ETX Client](../../doc/controllers/etx-registration.md#register-etx-client)
* [Renew ETX Client Certificate](../../doc/controllers/etx-registration.md#renew-etx-client-certificate)
* [Unregister ETX Clients](../../doc/controllers/etx-registration.md#unregister-etx-clients)
* [Get ETX Client Certificate](../../doc/controllers/etx-registration.md#get-etx-client-certificate)
* [Get ETX Connection Url](../../doc/controllers/etx-registration.md#get-etx-connection-url)
* [Get ETX Connection Url Multi Mec](../../doc/controllers/etx-registration.md#get-etx-connection-url-multi-mec)
* [Query ETX Devices](../../doc/controllers/etx-registration.md#query-etx-devices)


# Register ETX Client

With this API call the user (client) registers its device or software service to the ETX system. Therefore, when a connection is initiated from the device or software service to the ETX system along with the credential provided by this registration call, then the connection will be authorized.

- The user can register multiple devices or software services, which can all be used at the same time.
- There rules set in the system that limit the type and subtype of the clients that are allowed to be registered under the VendorID. The rules are created based ont he agreement between the Vendor and Verizon.
- The user will only be able to register a limited number of devices or software services under the same VendorID. This registration limit is specified by the agreement between the Vendor and Verizon.

Note: The user needs to authenticate with their ThingSpace credentials using the Access/Bearer and Session/M2M tokens in order to call this API.

```java
CompletableFuture<ApiResponse<ClientRegistrationResponse>> registerETXClientAsync(
    final ClientRegistrationRequestV2 body,
    final UUID xTransactionId)
```

## Authentication

This endpoint requires [thingspace_oauth](../../doc/auth/oauth-2-client-credentials-grant.md) **AND** [sessionToken](../../doc/auth/custom-header-signature-1.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`ClientRegistrationRequestV2`](../../doc/models/client-registration-request-v2.md) | Body, Required | - |
| `xTransactionId` | `UUID` | Header, Optional | Optional transaction identifier for tracing requests. If not provided, the application will generate one. |

## Server

`Server.IMP_SERVER`

## Response Type

**200**: Successful Registration

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ClientRegistrationResponse`](../../doc/models/client-registration-response.md).

## Example Usage

```java
ClientRegistrationRequestV2 body = new ClientRegistrationRequestV2.Builder(
    EtxClientTypeEnum.TRAFFICLIGHTCONTROLLER,
    ClientSubtypeEnum.SCOOTER,
    "VerizonETX"
)
.deviceID(UUID.fromString("a4fcd16a-343d-4527-8203-2f46e3e4ff4b"))
.iMEI("12-345678-901234-5")
.iCCID("89345678901234567890")
.iMSI("123456789012345")
.build();

UUID xTransactionId = UUID.fromString("123e4567-e89b-12d3-a456-426614174000");

eTXRegistrationController.registerETXClientAsync(body, xTransactionId).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof ETXRespondingErrorException) {
        ETXRespondingErrorException eTXRespondingErrorException = (ETXRespondingErrorException) cause;
        eTXRespondingErrorException.printStackTrace();
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
| 400 | Invalid Request | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| 401 | Unauthorized Request | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| 403 | Forbidden Request | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| 429 | Too Many Requests | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| 503 | Internal Server Error | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| Default | Forbidden | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |


# Renew ETX Client Certificate

With this API call the user (client) can:

- renew the certificate of a device or software service in the ETX system if the original certificate has expired. If the client's certificate expired or going to expire within 30 days and new certificate will be issued. If the certificate expires more than 30 days, the current certificate will be returned to the client.
- complete its device or software service registration to the ETX system if the original registration request was not successful because of a pending certificate generation. Whenever the user receives a "client registration is pending" response (HTTP 202) from POST /clients/registration call. The client should initiate this PUT API call to finish the registration process and get the required certificate.

Note: The user needs to authenticate with their ThingSpace credentials using the Access/Bearer and Session/M2M tokens in order to call this API.

```java
CompletableFuture<ApiResponse<ClientRegistrationResponse>> renewETXClientCertificateAsync(
    final UUID deviceID,
    final String vendorID,
    final UUID xTransactionId,
    final Object body)
```

## Authentication

This endpoint requires [thingspace_oauth](../../doc/auth/oauth-2-client-credentials-grant.md) **AND** [sessionToken](../../doc/auth/custom-header-signature-1.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deviceID` | `UUID` | Header, Required | - |
| `vendorID` | `String` | Header, Required | The VendorID set during the Vendor registration call.<br><br>**Constraints**: *Maximum Length*: `64`, *Pattern*: `^[a-zA-Z0-9]+$` |
| `xTransactionId` | `UUID` | Header, Optional | Optional transaction identifier for tracing requests. If not provided, the application will generate one. |
| `body` | `Object` | Body, Optional | - |

## Server

`Server.IMP_SERVER`

## Response Type

**200**: Successful Registration

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ClientRegistrationResponse`](../../doc/models/client-registration-response.md).

## Example Usage

```java
UUID deviceID = UUID.fromString("a4fcd16a-343d-4527-8203-2f46e3e4ff4b");
String vendorID = "VerizonETX";
UUID xTransactionId = UUID.fromString("123e4567-e89b-12d3-a456-426614174000");

eTXRegistrationController.renewETXClientCertificateAsync(deviceID, vendorID, xTransactionId, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof ETXRespondingErrorException) {
        ETXRespondingErrorException eTXRespondingErrorException = (ETXRespondingErrorException) cause;
        eTXRespondingErrorException.printStackTrace();
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
| 400 | Invalid Request | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| 401 | Unauthorized Request | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| 403 | Forbidden Request | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| 429 | Too Many Requests | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| 503 | Internal Server Error | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| Default | Forbidden | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |


# Unregister ETX Clients

With this API call the user (client) can unregister its devices and software services from the ETX system. The unregistered devices and services will no longer be able to use the ETX Message Exchange.

Note: The user needs to authenticate with their ThingSpace credentials using the Access/Bearer and Session/M2M tokens in order to call this API.

```java
CompletableFuture<ApiResponse<Void>> unregisterETXClientsAsync(
    final List<UUID> deviceIDs,
    final String vendorID,
    final UUID xTransactionId)
```

## Authentication

This endpoint requires [thingspace_oauth](../../doc/auth/oauth-2-client-credentials-grant.md) **AND** [sessionToken](../../doc/auth/custom-header-signature-1.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deviceIDs` | `List<UUID>` | Query, Required | The list of device IDs and software service IDs to be unregistered<br><br>**Constraints**: *Minimum Items*: `1`, *Maximum Items*: `100` |
| `vendorID` | `String` | Header, Required | The VendorID set during the Vendor registration call.<br><br>**Constraints**: *Maximum Length*: `64`, *Pattern*: `^[a-zA-Z0-9]+$` |
| `xTransactionId` | `UUID` | Header, Optional | Optional transaction identifier for tracing requests. If not provided, the application will generate one. |

## Server

`Server.IMP_SERVER`

## Response Type

**204**: Successful Deletion

`void`

## Example Usage

```java
List<UUID> deviceIDs = Arrays.asList(
    UUID.fromString("0000225a-0000-0000-0000-000000000000")
);

String vendorID = "VerizonETX";
UUID xTransactionId = UUID.fromString("123e4567-e89b-12d3-a456-426614174000");

eTXRegistrationController.unregisterETXClientsAsync(deviceIDs, vendorID, xTransactionId).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof ETXRespondingErrorException) {
        ETXRespondingErrorException eTXRespondingErrorException = (ETXRespondingErrorException) cause;
        eTXRespondingErrorException.printStackTrace();
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
| 400 | Invalid Request | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| 401 | Unauthorized Request | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| 403 | Forbidden Request | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| 429 | Too Many Requests | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| 503 | Internal Server Error | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| Default | Forbidden | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |


# Get ETX Client Certificate

With this API call the user can check the certificate of the device. At least one of the DeviceID, IMEI, ICCID or IMSI is required to make the call.

Note: The user needs to authenticate with their ThingSpace credentials using the Access/Bearer and Session/M2M tokens in order to call this API.

```java
CompletableFuture<ApiResponse<ClientPersistenceResponse>> getETXClientCertificateAsync(
    final ETXClientIDLookup iD,
    final String vendorID,
    final UUID xTransactionId)
```

## Authentication

This endpoint requires [thingspace_oauth](../../doc/auth/oauth-2-client-credentials-grant.md) **AND** [sessionToken](../../doc/auth/custom-header-signature-1.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `iD` | [`ETXClientIDLookup`](../../doc/models/etx-client-id-lookup.md) | Query, Required | One of the following IDs is required- DeviceID, IMEI, ICCID, IMSI. If more than one ID is provided, the API will return the certificate for the first ID found. The IDs are evaluated in the following order: DeviceID, IMEI, ICCID, IMSI. If the first provided ID is not found, the API will return an error. |
| `vendorID` | `String` | Header, Required | The VendorID set during the Vendor registration call.<br><br>**Constraints**: *Maximum Length*: `64`, *Pattern*: `^[a-zA-Z0-9]+$` |
| `xTransactionId` | `UUID` | Header, Optional | Optional transaction identifier for tracing requests. If not provided, the application will generate one. |

## Server

`Server.IMP_SERVER`

## Response Type

**200**: Successful retrieval

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ClientPersistenceResponse`](../../doc/models/client-persistence-response.md).

## Example Usage

```java
ETXClientIDLookup iD = new ETXClientIDLookup.Builder()
    .deviceID(UUID.fromString("a4fcd16a-343d-4527-8203-2f46e3e4ff4b"))
    .iMEI("12-345678-901234-5")
    .iCCID("89345678901234567890")
    .iMSI("123456789012345")
    .build();

String vendorID = "VerizonETX";
UUID xTransactionId = UUID.fromString("123e4567-e89b-12d3-a456-426614174000");

eTXRegistrationController.getETXClientCertificateAsync(iD, vendorID, xTransactionId).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof ETXRespondingErrorException) {
        ETXRespondingErrorException eTXRespondingErrorException = (ETXRespondingErrorException) cause;
        eTXRespondingErrorException.printStackTrace();
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
| 400 | Invalid request | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| 401 | Unauthorized | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| 403 | Forbidden Request | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| 404 | Not Found | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| 429 | Too Many Requests | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| 500 | Internal server Error | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| Default | Forbidden | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |


# Get ETX Connection Url

With this API call the device or software service requests the MQTT URL for the location that it needs to connect. To determine the proper URL the device or software service needs to provide its ID (the one that was provided in the registration request), location (GPS coordinates), and whether it is on the Verizon cellular network or not.

Note: The user needs to authenticate with their ThingSpace credentials using the Access/Bearer and Session/M2M tokens in order to call this API.

```java
CompletableFuture<ApiResponse<ConnectionResponse>> getETXConnectionUrlAsync(
    final String vendorID,
    final ConnectionRequest body,
    final UUID xTransactionId)
```

## Authentication

This endpoint requires [thingspace_oauth](../../doc/auth/oauth-2-client-credentials-grant.md) **AND** [sessionToken](../../doc/auth/custom-header-signature-1.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vendorID` | `String` | Header, Required | The VendorID set during the Vendor registration call.<br><br>**Constraints**: *Maximum Length*: `64`, *Pattern*: `^[a-zA-Z0-9]+$` |
| `body` | [`ConnectionRequest`](../../doc/models/connection-request.md) | Body, Required | - |
| `xTransactionId` | `UUID` | Header, Optional | Optional transaction identifier for tracing requests. If not provided, the application will generate one. |

## Server

`Server.IMP_SERVER`

## Response Type

**200**: Successful retrieval

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ConnectionResponse`](../../doc/models/connection-response.md).

## Example Usage

```java
String vendorID = "VerizonETX";
ConnectionRequest body = new ConnectionRequest.Builder(
    UUID.fromString("976c4bad-03d3-4dcb-9688-ee57db7890e4"),
    new Geolocation.Builder(
        42.36D,
        -71.06D
    )
    .build(),
    NetworkTypeEnum.NONVZ
)
.build();

UUID xTransactionId = UUID.fromString("123e4567-e89b-12d3-a456-426614174000");

eTXRegistrationController.getETXConnectionUrlAsync(vendorID, body, xTransactionId).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof ETXRespondingErrorException) {
        ETXRespondingErrorException eTXRespondingErrorException = (ETXRespondingErrorException) cause;
        eTXRespondingErrorException.printStackTrace();
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
| 400 | Invalid request | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| 401 | Unauthorized | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| 403 | Forbidden Request | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| 429 | Too Many Requests | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| 503 | Internal server Error | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| Default | Forbidden | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |


# Get ETX Connection Url Multi Mec

With this API call the device or software service requests the MQTT URL for the location that it needs to connect. To determine the proper URL the device or software service needs to provide its ID (the one that was provided in the registration request), location (GPS coordinates), and whether it is on the Verizon cellular network or not.

If there are multiple MECs that serve the location of the client all options are provided in the response, and the client is free to choose which MEC they want to connect.

Note: The user needs to authenticate with their ThingSpace credentials using the Access/Bearer and Session/M2M tokens in order to call this API.

```java
CompletableFuture<ApiResponse<ConnectionResponseV3>> getETXConnectionUrlMultiMecAsync(
    final String vendorID,
    final ConnectionRequest body,
    final UUID xTransactionId)
```

## Authentication

This endpoint requires [thingspace_oauth](../../doc/auth/oauth-2-client-credentials-grant.md) **AND** [sessionToken](../../doc/auth/custom-header-signature-1.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vendorID` | `String` | Header, Required | The VendorID set during the Vendor registration call.<br><br>**Constraints**: *Maximum Length*: `64`, *Pattern*: `^[a-zA-Z0-9]+$` |
| `body` | [`ConnectionRequest`](../../doc/models/connection-request.md) | Body, Required | - |
| `xTransactionId` | `UUID` | Header, Optional | Optional transaction identifier for tracing requests. If not provided, the application will generate one. |

## Server

`Server.IMP_SERVER`

## Response Type

**200**: Successful retrieval

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ConnectionResponseV3`](../../doc/models/connection-response-v3.md).

## Example Usage

```java
String vendorID = "VerizonETX";
ConnectionRequest body = new ConnectionRequest.Builder(
    UUID.fromString("976c4bad-03d3-4dcb-9688-ee57db7890e4"),
    new Geolocation.Builder(
        42.36D,
        -71.06D
    )
    .build(),
    NetworkTypeEnum.NONVZ
)
.build();

UUID xTransactionId = UUID.fromString("123e4567-e89b-12d3-a456-426614174000");

eTXRegistrationController.getETXConnectionUrlMultiMecAsync(vendorID, body, xTransactionId).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof ETXRespondingErrorException) {
        ETXRespondingErrorException eTXRespondingErrorException = (ETXRespondingErrorException) cause;
        eTXRespondingErrorException.printStackTrace();
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
| 400 | Invalid request | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| 401 | Unauthorized | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| 403 | Forbidden Request | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| 429 | Too Many Requests | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| 503 | Internal server Error | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| Default | Forbidden | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |


# Query ETX Devices

This API allows retrieving devices by vendor ID and optional filters. The request should include the VendorID and any filters to apply.

```java
CompletableFuture<ApiResponse<List<DevicesResponse>>> queryETXDevicesAsync(
    final DevicesRequest body,
    final UUID xTransactionId)
```

## Authentication

This endpoint requires [thingspace_oauth](../../doc/auth/oauth-2-client-credentials-grant.md) **AND** [sessionToken](../../doc/auth/custom-header-signature-1.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`DevicesRequest`](../../doc/models/devices-request.md) | Body, Required | - |
| `xTransactionId` | `UUID` | Header, Optional | Optional transaction identifier for tracing requests. If not provided, the application will generate one. |

## Server

`Server.IMP_SERVER`

## Response Type

**200**: Successful retrieval of devices

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`List<DevicesResponse>`](../../doc/models/devices-response.md).

## Example Usage

```java
DevicesRequest body = new DevicesRequest.Builder(
    "VerizonETX"
)
.build();

UUID xTransactionId = UUID.fromString("123e4567-e89b-12d3-a456-426614174000");

eTXRegistrationController.queryETXDevicesAsync(body, xTransactionId).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof ETXRespondingErrorException) {
        ETXRespondingErrorException eTXRespondingErrorException = (ETXRespondingErrorException) cause;
        eTXRespondingErrorException.printStackTrace();
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
| 400 | Invalid Request | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| 401 | Unauthorized Request | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| 500 | Internal Server Error | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |
| Default | Forbidden | [`ETXRespondingErrorException`](../../doc/models/etx-responding-error-exception.md) |

