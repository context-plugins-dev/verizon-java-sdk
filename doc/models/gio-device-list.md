
# GIO Device List

## Structure

`GIODeviceList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceIds` | [`List<GIODeviceId>`](../../doc/models/gio-device-id.md) | Optional | **Constraints**: *Maximum Items*: `100` | List<GIODeviceId> getDeviceIds() | setDeviceIds(List<GIODeviceId> deviceIds) |

## Example

```java
import com.verizon.thingspace.models.GIODeviceId;
import com.verizon.thingspace.models.GIODeviceList;
import java.util.Arrays;

GIODeviceList gIODeviceList = new GIODeviceList.Builder()
    .deviceIds(Arrays.asList(
        new GIODeviceId.Builder(
            "kind8",
            "id0"
        )
        .build()
    ))
    .build();
```

