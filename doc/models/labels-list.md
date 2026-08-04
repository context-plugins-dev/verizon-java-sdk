
# Labels List

## Structure

`LabelsList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceIds` | [`List<LabelsListDeviceIds>`](../../doc/models/containers/labels-list-device-ids.md) | Optional | This is List of a container for any-of cases.<br><br>**Constraints**: *Maximum Items*: `100` | List<LabelsListDeviceIds> getDeviceIds() | setDeviceIds(List<LabelsListDeviceIds> deviceIds) |

## Example

```java
import com.verizon.thingspace.models.DeviceLabels;
import com.verizon.thingspace.models.LabelsList;
import com.verizon.thingspace.models.containers.LabelsListDeviceIds;
import java.util.Arrays;

LabelsList labelsList = new LabelsList.Builder()
    .deviceIds(Arrays.asList(
        LabelsListDeviceIds.fromDeviceLabels(
            new DeviceLabels.Builder(
                "name6",
                "value8"
            )
            .build()
        )
    ))
    .build();
```

