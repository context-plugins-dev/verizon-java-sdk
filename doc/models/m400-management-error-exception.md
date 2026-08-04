
# M400 Management Error Exception

## Structure

`M400ManagementErrorException`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Error` | `String` | Optional | - | String getError() | setError(String error) |
| `ErrorDescription` | `String` | Optional | **Constraints**: *Maximum Length*: `1000` | String getErrorDescription() | setErrorDescription(String errorDescription) |
| `Cause` | `String` | Optional | - | String getCauseField() | setCauseField(String causeField) |

## Example

```java
try {
    // make the API call
} catch (M400ManagementErrorException e) {
    e.printStackTrace();
} catch (ApiException e) {
    e.printStackTrace();
}
```

