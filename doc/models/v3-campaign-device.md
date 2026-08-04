
# V3 Campaign Device

Campaign history.

## Structure

`V3CampaignDevice`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `TotalDevice` | `Integer` | Optional | Total device count. | Integer getTotalDevice() | setTotalDevice(Integer totalDevice) |
| `HasMoreData` | `boolean` | Required | Has more report flag. | boolean getHasMoreData() | setHasMoreData(boolean hasMoreData) |
| `LastSeenDeviceId` | `String` | Optional | Device identifier. | String getLastSeenDeviceId() | setLastSeenDeviceId(String lastSeenDeviceId) |
| `MaxPageSize` | `int` | Required | Maximum page size. | int getMaxPageSize() | setMaxPageSize(int maxPageSize) |
| `DeviceList` | [`List<V3DeviceStatus>`](../../doc/models/v3-device-status.md) | Required | List of devices with id in IMEI. | List<V3DeviceStatus> getDeviceList() | setDeviceList(List<V3DeviceStatus> deviceList) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.V3CampaignDevice;
import com.verizon.thingspace.models.V3DeviceStatus;
import java.util.Arrays;

V3CampaignDevice v3CampaignDevice = new V3CampaignDevice.Builder(
    true,
    1000,
    Arrays.asList(
        new V3DeviceStatus.Builder(
            "15-digit IMEI",
            "UpgradePending"
        )
        .resultReason("Upgrade pending, the device upgrade is estimated to be scheduled for 06 Oct 22 18:05 UTC")
        .updatedTime(DateTimeHelper.fromRfc8601DateTime("2022-08-05T21:05:27.129Z"))
        .recentAttemptTime(DateTimeHelper.fromRfc8601DateTime("2022-10-05T21:05:01.19Z"))
        .nextAttemptTime(DateTimeHelper.fromRfc8601DateTime("2022-10-06T18:35:00Z"))
        .build()
    )
)
.totalDevice(2689)
.lastSeenDeviceId("15-digit IMEI")
.build();
```

