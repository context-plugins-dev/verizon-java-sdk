
# Tscore

## Structure

`Tscore`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Profileid` | `String` | Optional | the UUID of the profile | String getProfileid() | setProfileid(String profileid) |
| `Profileversionid` | `String` | Optional | the UUID of the profile version | String getProfileversionid() | setProfileversionid(String profileversionid) |

## Example

```java
import com.verizon.thingspace.models.Tscore;

Tscore tscore = new Tscore.Builder()
    .profileid("the UUID of the profile")
    .profileversionid("the UUID of the profile version")
    .build();
```

