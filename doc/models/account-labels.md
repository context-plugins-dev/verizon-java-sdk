
# Account Labels

Maximum of 2,000 objects are allowed in the array.

## Structure

`AccountLabels`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Devices` | [`List<DeviceList>`](../../doc/models/device-list.md) | Required | - | List<DeviceList> getDevices() | setDevices(List<DeviceList> devices) |
| `Label` | [`List<DeviceLabels>`](../../doc/models/device-labels.md) | Optional | - | List<DeviceLabels> getLabel() | setLabel(List<DeviceLabels> label) |

## Example

```java
import com.verizon.thingspace.models.AccountLabels;
import com.verizon.thingspace.models.DeviceId;
import com.verizon.thingspace.models.DeviceLabels;
import com.verizon.thingspace.models.DeviceList;
import java.util.Arrays;

AccountLabels accountLabels = new AccountLabels.Builder(
    Arrays.asList(
        new DeviceList.Builder()
            .deviceIds(Arrays.asList(
                new DeviceId.Builder(
                    "id0",
                    "kind8"
                )
                .build()
            ))
            .build()
    )
)
.label(Arrays.asList(
        new DeviceLabels.Builder(
            "name0",
            "value2"
        )
        .build(),
        new DeviceLabels.Builder(
            "name0",
            "value2"
        )
        .build(),
        new DeviceLabels.Builder(
            "name0",
            "value2"
        )
        .build()
    ))
.build();
```

