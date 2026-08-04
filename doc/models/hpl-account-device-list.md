
# Hpl Account Device List

A list of device IDs

## Structure

`HplAccountDeviceList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceIds` | [`List<HplDeviceId>`](../../doc/models/hpl-device-id.md) | Optional | - | List<HplDeviceId> getDeviceIds() | setDeviceIds(List<HplDeviceId> deviceIds) |

## Example

```java
import com.verizon.thingspace.models.HplAccountDeviceList;
import com.verizon.thingspace.models.HplDeviceId;
import java.util.Arrays;

HplAccountDeviceList hplAccountDeviceList = new HplAccountDeviceList.Builder()
    .deviceIds(Arrays.asList(
        new HplDeviceId.Builder()
            .kind("kind8")
            .id("id0")
            .build(),
        new HplDeviceId.Builder()
            .kind("kind8")
            .id("id0")
            .build()
    ))
    .build();
```

