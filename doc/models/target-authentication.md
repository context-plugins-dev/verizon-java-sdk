
# Target Authentication

OAuth 2 token and refresh token for TS to stream events to Target.

## Structure

`TargetAuthentication`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Body` | [`TargetAuthenticationBody`](../../doc/models/target-authentication-body.md) | Optional | - | TargetAuthenticationBody getBody() | setBody(TargetAuthenticationBody body) |
| `Version` | `String` | Optional | - | String getVersion() | setVersion(String version) |

## Example

```java
import com.verizon.thingspace.models.TargetAuthentication;
import com.verizon.thingspace.models.TargetAuthenticationBody;
import com.verizon.thingspace.models.TargetAuthenticationBodyHeaders;
import com.verizon.thingspace.models.TargetAuthenticationBodyHost;

TargetAuthentication targetAuthentication = new TargetAuthentication.Builder()
    .body(new TargetAuthenticationBody.Builder()
        .grantType("refresh_token")
        .refreshToken("qfeqVjZTYzMmUtZWMzZqfq4ZDUtNzFhZWVkYTlmMjk1")
        .scope("scope6")
        .headers(new TargetAuthenticationBodyHeaders.Builder()
            .authorization("Basic RGFrqewfq2xpZW50QXBwVjI6YzM5YjqfqmI2LWI2MWQtNDRlZTQ5MmM1YTRk")
            .contentType("application/x-www-form-urlencoded")
            .build())
        .host(new TargetAuthenticationBodyHost.Builder()
            .hostandpath("https:// myhost.com:1825")
            .build())
        .build())
    .version("1.0")
    .build();
```

