
# V3 Software Info

Software information.

## Structure

`V3SoftwareInfo`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | Software name. | String getName() | setName(String name) |
| `Version` | `String` | Required | Software version. | String getVersion() | setVersion(String version) |
| `UpgradeTime` | `String` | Required | Upgrade time. | String getUpgradeTime() | setUpgradeTime(String upgradeTime) |

## Example

```java
import com.verizon.thingspace.models.V3SoftwareInfo;

V3SoftwareInfo v3SoftwareInfo = new V3SoftwareInfo.Builder(
    "VZ_MDM_IOT",
    "0.14",
    "2012-04-23T18:25:43.511Z"
)
.build();
```

