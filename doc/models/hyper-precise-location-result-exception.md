
# Hyper Precise Location Result Exception

Error response.

## Structure

`HyperPreciseLocationResultException`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ResponseCode` | [`ErrorResponseCodeEnum`](../../doc/models/error-response-code-enum.md) | Optional | Error Code. | ErrorResponseCodeEnum getResponseCodeField() | setResponseCodeField(ErrorResponseCodeEnum responseCodeField) |
| `Message` | `String` | Optional | Error message. | String getMessageField() | setMessageField(String messageField) |
| `Fault` | [`HyperPreciseLocationFault`](../../doc/models/hyper-precise-location-fault.md) | Optional | Fault occurred while responding. | HyperPreciseLocationFault getFault() | setFault(HyperPreciseLocationFault fault) |

## Example

```java
try {
    // make the API call
} catch (HyperPreciseLocationResultException e) {
    e.printStackTrace();
} catch (ApiException e) {
    e.printStackTrace();
}
```

