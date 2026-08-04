
# Deactivate Device List

## Structure

`DeactivateDeviceList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Ids` | [`List<DeactivateDeviceListIds>`](../../doc/models/containers/deactivate-device-list-ids.md) | Optional | This is List of a container for any-of cases.<br><br>**Constraints**: *Maximum Items*: `100` | List<DeactivateDeviceListIds> getIds() | setIds(List<DeactivateDeviceListIds> ids) |

## Example

```java
import com.verizon.thingspace.models.DeactivateDeviceList;
import com.verizon.thingspace.models.DeviceId;
import com.verizon.thingspace.models.containers.DeactivateDeviceListIds;
import java.util.Arrays;

DeactivateDeviceList deactivateDeviceList = new DeactivateDeviceList.Builder()
    .ids(Arrays.asList(
        DeactivateDeviceListIds.fromDeviceId(
            new DeviceId.Builder(
                "id2",
                "kind0"
            )
            .build()
        ),
        DeactivateDeviceListIds.fromDeviceId(
            new DeviceId.Builder(
                "id2",
                "kind0"
            )
            .build()
        ),
        DeactivateDeviceListIds.fromDeviceId(
            new DeviceId.Builder(
                "id2",
                "kind0"
            )
            .build()
        )
    ))
    .build();
```

