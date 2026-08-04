
# Session Reset Password Request

Request to a new, randomly generated password for the current username.

## Structure

`SessionResetPasswordRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `OldPassword` | `String` | Required | The current password for the username. | String getOldPassword() | setOldPassword(String oldPassword) |

## Example

```java
import com.verizon.thingspace.models.SessionResetPasswordRequest;

SessionResetPasswordRequest sessionResetPasswordRequest = new SessionResetPasswordRequest.Builder(
    "grflbk"
)
.build();
```

