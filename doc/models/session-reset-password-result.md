
# Session Reset Password Result

Response to a new, randomly generated password for the current username.

## Structure

`SessionResetPasswordResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NewPassword` | `String` | Optional | The new password for the username. | String getNewPassword() | setNewPassword(String newPassword) |

## Example

```java
import com.verizon.thingspace.models.SessionResetPasswordResult;

SessionResetPasswordResult sessionResetPasswordResult = new SessionResetPasswordResult.Builder()
    .newPassword("Wh0a1545a84d")
    .build();
```

