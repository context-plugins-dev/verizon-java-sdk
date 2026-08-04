
# Connectivity Management Result Exception

Response to errors.

## Structure

`ConnectivityManagementResultException`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ErrorCode` | `String` | Optional | Code of the error. | String getErrorCode() | setErrorCode(String errorCode) |
| `ErrorMessage` | `String` | Optional | Details of the error. | String getErrorMessage() | setErrorMessage(String errorMessage) |

## Example

```java
try {
    // make the API call
} catch (ConnectivityManagementResultException e) {
    e.printStackTrace();
} catch (ApiException e) {
    e.printStackTrace();
}
```

