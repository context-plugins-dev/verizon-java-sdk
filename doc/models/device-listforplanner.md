
# Device Listforplanner

## Structure

`DeviceListforplanner`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceIds` | [`List<DeviceIdforplanner>`](../../doc/models/device-idforplanner.md) | Optional | - | List<DeviceIdforplanner> getDeviceIds() | setDeviceIds(List<DeviceIdforplanner> deviceIds) |
| `PrivateNetworkApns` | [`List<PrivateNetworkApns>`](../../doc/models/private-network-apns.md) | Optional | - | List<PrivateNetworkApns> getPrivateNetworkApns() | setPrivateNetworkApns(List<PrivateNetworkApns> privateNetworkApns) |
| `Ipaddress` | `String` | Optional | A IPv4 address | String getIpaddress() | setIpaddress(String ipaddress) |
| `ActivationCode` | `String` | Optional | The activation code value. | String getActivationCode() | setActivationCode(String activationCode) |

## Example

```java
import com.verizon.thingspace.models.DeviceIdforplanner;
import com.verizon.thingspace.models.DeviceListforplanner;
import com.verizon.thingspace.models.PrivateNetworkApns;
import java.util.Arrays;

DeviceListforplanner deviceListforplanner = new DeviceListforplanner.Builder()
    .deviceIds(Arrays.asList(
        new DeviceIdforplanner.Builder()
            .kind("kind8")
            .id("id0")
            .build(),
        new DeviceIdforplanner.Builder()
            .kind("kind8")
            .id("id0")
            .build(),
        new DeviceIdforplanner.Builder()
            .kind("kind8")
            .id("id0")
            .build()
    ))
    .privateNetworkApns(Arrays.asList(
        new PrivateNetworkApns.Builder()
            .apnName("apnName2")
            .addressAssignmentMethod("addressAssignmentMethod8")
            .ipaddress("ipAddress4")
            .build(),
        new PrivateNetworkApns.Builder()
            .apnName("apnName2")
            .addressAssignmentMethod("addressAssignmentMethod8")
            .ipaddress("ipAddress4")
            .build()
    ))
    .ipaddress("10.10.10.01")
    .activationCode("activationCode2")
    .build();
```

