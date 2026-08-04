
# Activate

## Structure

`Activate`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Profile` | `String` | Required | - | String getProfile() | setProfile(String profile) |

## Example

```java
import com.verizon.thingspace.models.Activate;

Activate activate = new Activate.Builder(
    "HSS EsmProfile Enterprise 5G"
)
.build();
```

