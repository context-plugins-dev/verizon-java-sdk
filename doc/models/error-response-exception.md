
# Error Response Exception

## Structure

`ErrorResponseException`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ResponseCode` | `String` | Optional | - | String getResponseCodeField() | setResponseCodeField(String responseCodeField) |
| `Message` | `String` | Optional | - | String getMessageField() | setMessageField(String messageField) |

## Example

```java
try {
    // make the API call
} catch (ErrorResponseException e) {
    e.printStackTrace();
} catch (ApiException e) {
    e.printStackTrace();
}
```

