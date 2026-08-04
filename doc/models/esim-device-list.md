
# ESIM Device List

## Structure

`ESIMDeviceList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceIds` | [`List<ESIMDeviceListDeviceIds>`](../../doc/models/containers/esim-device-list-device-ids.md) | Optional | This is List of a container for any-of cases.<br><br>**Constraints**: *Maximum Items*: `100` | List<ESIMDeviceListDeviceIds> getDeviceIds() | setDeviceIds(List<ESIMDeviceListDeviceIds> deviceIds) |

## Example

```java
import com.verizon.thingspace.models.ESIMDeviceId;
import com.verizon.thingspace.models.ESIMDeviceList;
import com.verizon.thingspace.models.containers.ESIMDeviceListDeviceIds;
import java.util.Arrays;

ESIMDeviceList eSIMDeviceList = new ESIMDeviceList.Builder()
    .deviceIds(Arrays.asList(
        ESIMDeviceListDeviceIds.fromESIMDeviceId(
            new ESIMDeviceId.Builder()
                .id("id4")
                .kind("kind2")
                .build()
        )
    ))
    .build();
```

