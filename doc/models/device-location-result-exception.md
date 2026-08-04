
# Device Location Result Exception

Will be empty if there was no error.

## Structure

`DeviceLocationResultException`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ErrorCode` | `String` | Required | - | String getErrorCode() | setErrorCode(String errorCode) |
| `ErrorMessage` | `String` | Required | - | String getErrorMessage() | setErrorMessage(String errorMessage) |

## Example

```java
try {
    // make the API call
} catch (DeviceLocationResultException e) {
    e.printStackTrace();
} catch (ApiException e) {
    e.printStackTrace();
}
```

