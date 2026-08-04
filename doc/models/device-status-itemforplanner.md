
# Device Status Itemforplanner

## Structure

`DeviceStatusItemforplanner`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceIds` | [`List<DeviceIdforplanner>`](../../doc/models/device-idforplanner.md) | Optional | - | List<DeviceIdforplanner> getDeviceIds() | setDeviceIds(List<DeviceIdforplanner> deviceIds) |
| `Status` | `String` | Optional | - | String getStatus() | setStatus(String status) |
| `Reason` | `String` | Optional | - | String getReason() | setReason(String reason) |

## Example

```java
import com.verizon.thingspace.models.DeviceIdforplanner;
import com.verizon.thingspace.models.DeviceStatusItemforplanner;
import java.util.Arrays;

DeviceStatusItemforplanner deviceStatusItemforplanner = new DeviceStatusItemforplanner.Builder()
    .deviceIds(Arrays.asList(
        new DeviceIdforplanner.Builder()
            .kind("kind8")
            .id("id0")
            .build(),
        new DeviceIdforplanner.Builder()
            .kind("kind8")
            .id("id0")
            .build()
    ))
    .status("status6")
    .reason("reason0")
    .build();
```

