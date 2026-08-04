
# Fota V3 Result Exception

Error response.

## Structure

`FotaV3ResultException`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ErrorCode` | `String` | Required | Error code string. | String getErrorCode() | setErrorCode(String errorCode) |
| `ErrorMessage` | `String` | Required | Error message string. | String getErrorMessage() | setErrorMessage(String errorMessage) |

## Example

```java
try {
    // make the API call
} catch (FotaV3ResultException e) {
    e.printStackTrace();
} catch (ApiException e) {
    e.printStackTrace();
}
```

