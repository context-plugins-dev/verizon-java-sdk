
# Mdm Error Response Exception

error response structure

## Structure

`MdmErrorResponseException`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Error` | `String` | Required | The short summary of the error<br><br>**Constraints**: *Maximum Length*: `1024`, *Pattern*: `^[a-zA-Z0-9_-]+$` | String getError() | setError(String error) |
| `Description` | `String` | Required | The detailed description of the error<br><br>**Constraints**: *Maximum Length*: `4096`, *Pattern*: `^[a-zA-Z0-9_-]+$` | String getDescription() | setDescription(String description) |
| `Uuid` | `UUID` | Required | The unique identifier of the request for tracing | UUID getUuid() | setUuid(UUID uuid) |
| `Timestamp` | `LocalDateTime` | Required | The timestamp of when the error occurred | LocalDateTime getTimestamp() | setTimestamp(LocalDateTime timestamp) |

## Example

```java
try {
    // make the API call
} catch (MdmErrorResponseException e) {
    e.printStackTrace();
} catch (ApiException e) {
    e.printStackTrace();
}
```

