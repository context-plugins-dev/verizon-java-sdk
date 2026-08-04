
# Target Authentication Body

## Structure

`TargetAuthenticationBody`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `GrantType` | `String` | Optional | Authentication grant type. | String getGrantType() | setGrantType(String grantType) |
| `RefreshToken` | `String` | Optional | Refresh token. | String getRefreshToken() | setRefreshToken(String refreshToken) |
| `Scope` | `String` | Optional | Authentication scopes. | String getScope() | setScope(String scope) |
| `Headers` | [`TargetAuthenticationBodyHeaders`](../../doc/models/target-authentication-body-headers.md) | Optional | Authentication headers. | TargetAuthenticationBodyHeaders getHeaders() | setHeaders(TargetAuthenticationBodyHeaders headers) |
| `Host` | [`TargetAuthenticationBodyHost`](../../doc/models/target-authentication-body-host.md) | Optional | Host information. | TargetAuthenticationBodyHost getHost() | setHost(TargetAuthenticationBodyHost host) |

## Example

```java
import com.verizon.thingspace.models.TargetAuthenticationBody;
import com.verizon.thingspace.models.TargetAuthenticationBodyHeaders;
import com.verizon.thingspace.models.TargetAuthenticationBodyHost;

TargetAuthenticationBody targetAuthenticationBody = new TargetAuthenticationBody.Builder()
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
    .build();
```

