
# Fota V1 Result Exception

Response in case of any errors.

## Structure

`FotaV1ResultException`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ErrorCode` | `String` | Required | Error response code. | String getErrorCode() | setErrorCode(String errorCode) |
| `ErrorMessage` | `String` | Required | Description of the error. | String getErrorMessage() | setErrorMessage(String errorMessage) |

## Example

```java
try {
    // make the API call
} catch (FotaV1ResultException e) {
    e.printStackTrace();
} catch (ApiException e) {
    e.printStackTrace();
}
```

