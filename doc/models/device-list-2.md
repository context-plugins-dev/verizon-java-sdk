
# Device List 2

## Structure

`DeviceList2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Ids` | [`List<DeviceList2Ids>`](../../doc/models/containers/device-list-2-ids.md) | Optional | This is List of a container for any-of cases.<br><br>**Constraints**: *Maximum Items*: `100` | List<DeviceList2Ids> getIds() | setIds(List<DeviceList2Ids> ids) |

## Example

```java
import com.verizon.thingspace.models.DeviceList2;
import com.verizon.thingspace.models.ESIMDeviceId;
import com.verizon.thingspace.models.containers.DeviceList2Ids;
import java.util.Arrays;

DeviceList2 deviceList2 = new DeviceList2.Builder()
    .ids(Arrays.asList(
        DeviceList2Ids.fromESIMDeviceId(
            new ESIMDeviceId.Builder()
                .id("id4")
                .kind("kind2")
                .build()
        )
    ))
    .build();
```

