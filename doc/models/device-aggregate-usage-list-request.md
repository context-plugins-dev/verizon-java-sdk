
# Device Aggregate Usage List Request

Request to list device aggregate usage.

## Structure

`DeviceAggregateUsageListRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `StartTime` | `String` | Required | The beginning of the reporting period. The startTime cannot be more than 6 months before the current date. | String getStartTime() | setStartTime(String startTime) |
| `EndTime` | `String` | Required | The end of the reporting period. The endTime date must be within on month of the startTime date. | String getEndTime() | setEndTime(String endTime) |
| `DeviceIds` | [`List<DeviceId>`](../../doc/models/device-id.md) | Optional | One or more devices for which you want aggregate data, specified by device ID. | List<DeviceId> getDeviceIds() | setDeviceIds(List<DeviceId> deviceIds) |
| `AccountName` | `String` | Optional | The name of a billing account. | String getAccountName() | setAccountName(String accountName) |
| `GroupName` | `String` | Optional | The name of a device group, if you want to only include devices in that group. | String getGroupName() | setGroupName(String groupName) |
| `Label` | [`List<Label>`](../../doc/models/label.md) | Optional | **Constraints**: *Maximum Items*: `50` | List<Label> getLabel() | setLabel(List<Label> label) |

## Example

```java
import com.verizon.thingspace.models.DeviceAggregateUsageListRequest;
import com.verizon.thingspace.models.DeviceId;
import com.verizon.thingspace.models.Label;
import java.util.Arrays;

DeviceAggregateUsageListRequest deviceAggregateUsageListRequest = new DeviceAggregateUsageListRequest.Builder(
    "2021-08-01T00:00:00-06:00",
    "2021-08-30T00:00:00-06:00"
)
.deviceIds(Arrays.asList(
        new DeviceId.Builder(
            "84258000000891490087",
            "ICCID"
        )
        .build()
    ))
.accountName("9992330389-00001")
.groupName("groupName4")
.label(Arrays.asList(
        new Label.Builder()
            .name("name0")
            .value("value2")
            .build()
    ))
.build();
```

