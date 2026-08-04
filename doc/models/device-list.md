
# Device List

## Structure

`DeviceList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceIds` | [`List<DeviceId>`](../../doc/models/device-id.md) | Optional | **Constraints**: *Maximum Items*: `100` | List<DeviceId> getDeviceIds() | setDeviceIds(List<DeviceId> deviceIds) |

## Example

```java
import com.verizon.thingspace.models.DeviceId;
import com.verizon.thingspace.models.DeviceList;
import java.util.Arrays;

DeviceList deviceList = new DeviceList.Builder()
    .deviceIds(Arrays.asList(
        new DeviceId.Builder(
            "id0",
            "kind8"
        )
        .build()
    ))
    .build();
```

