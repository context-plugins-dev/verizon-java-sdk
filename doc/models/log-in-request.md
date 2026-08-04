
# Log In Request

Request to initiate a Connectivity Management session and returns a VZ-M2M session token that is required in subsequent API requests.

## Structure

`LogInRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Username` | `String` | Required | The username for authentication. | String getUsername() | setUsername(String username) |
| `Password` | `String` | Required | The password for authentication. | String getPassword() | setPassword(String password) |

## Example

```java
import com.verizon.thingspace.models.LogInRequest;

LogInRequest logInRequest = new LogInRequest.Builder(
    "zbeeblebrox",
    "IMgr8"
)
.build();
```

