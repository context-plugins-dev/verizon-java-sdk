
# Rest Error Responseforplanner Exception

## Structure

`RestErrorResponseforplannerException`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ErrorCode` | `String` | Optional | - | String getErrorCode() | setErrorCode(String errorCode) |
| `ErrorMessage` | `String` | Optional | - | String getErrorMessage() | setErrorMessage(String errorMessage) |
| `ErrorUrl` | `String` | Optional | - | String getErrorUrl() | setErrorUrl(String errorUrl) |

## Example

```java
try {
    // make the API call
} catch (RestErrorResponseforplannerException e) {
    e.printStackTrace();
} catch (ApiException e) {
    e.printStackTrace();
}
```

