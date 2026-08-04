
# Target Authentication Body Host

Host information.

## Structure

`TargetAuthenticationBodyHost`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Hostandpath` | `String` | Optional | - | String getHostandpath() | setHostandpath(String hostandpath) |

## Example

```java
import com.verizon.thingspace.models.TargetAuthenticationBodyHost;

TargetAuthenticationBodyHost targetAuthenticationBodyHost = new TargetAuthenticationBodyHost.Builder()
    .hostandpath("https:// myhost.com:1825")
    .build();
```

