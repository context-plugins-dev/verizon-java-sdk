
# Auth Sub Rest Error Responseforplanner

## Structure

`AuthSubRestErrorResponseforplanner`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Code` | `String` | Optional | - | String getCode() | setCode(String code) |
| `Message` | `String` | Optional | - | String getMessage() | setMessage(String message) |
| `Description` | `String` | Optional | - | String getDescription() | setDescription(String description) |

## Example

```java
import com.verizon.thingspace.models.AuthSubRestErrorResponseforplanner;

AuthSubRestErrorResponseforplanner authSubRestErrorResponseforplanner = new AuthSubRestErrorResponseforplanner.Builder()
    .code("code8")
    .message("message0")
    .description("description0")
    .build();
```

