
# Register Callback Request

Request to register a callback.

## Structure

`RegisterCallbackRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | The name of the callback service that you want to subscribe to. | String getName() | setName(String name) |
| `Url` | `String` | Required | The address on your server where you have enabled a listening service for callback messages. | String getUrl() | setUrl(String url) |
| `Username` | `String` | Optional | The user name that the M2M Platform should return in the callback messages. | String getUsername() | setUsername(String username) |
| `Password` | `String` | Optional | The password that the M2M Platform should return in the callback messages. | String getPassword() | setPassword(String password) |

## Example

```java
import com.verizon.thingspace.models.RegisterCallbackRequest;

RegisterCallbackRequest registerCallbackRequest = new RegisterCallbackRequest.Builder(
    "CarrierService",
    "https://mock.thingspace.verizon.com/webhook"
)
.username("username4")
.password("password8")
.build();
```

