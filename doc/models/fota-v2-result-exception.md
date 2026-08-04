
# Fota V2 Result Exception

Response for error cases.

## Structure

`FotaV2ResultException`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ErrorCode` | `String` | Required | Code of the error. | String getErrorCode() | setErrorCode(String errorCode) |
| `ErrorMessage` | `String` | Required | Details of the error. | String getErrorMessage() | setErrorMessage(String errorMessage) |

## Example

```java
try {
    // make the API call
} catch (FotaV2ResultException e) {
    e.printStackTrace();
} catch (ApiException e) {
    e.printStackTrace();
}
```

