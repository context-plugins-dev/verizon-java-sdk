
# Log In Result

Response to initiate a Connectivity Management session and returns a VZ-M2M session token that is required in subsequent API requests.

## Structure

`LogInResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SessionToken` | `String` | Optional | The identifier for the session that was created by the request. Store the sessionToken for use in the header of all other API requests. | String getSessionToken() | setSessionToken(String sessionToken) |

## Example

```java
import com.verizon.thingspace.models.LogInResult;

LogInResult logInResult = new LogInResult.Builder()
    .sessionToken("bcce3ea6-fe4f-4952-bacf-eadd80718e83")
    .build();
```

