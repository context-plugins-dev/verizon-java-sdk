
# V2 Campaign Device

List of devices in a campaign.

## Structure

`V2CampaignDevice`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `TotalDevice` | `Integer` | Optional | Total device count. | Integer getTotalDevice() | setTotalDevice(Integer totalDevice) |
| `HasMoreData` | `boolean` | Required | Has more report flag. | boolean getHasMoreData() | setHasMoreData(boolean hasMoreData) |
| `LastSeenDeviceId` | `String` | Optional | Device identifier. | String getLastSeenDeviceId() | setLastSeenDeviceId(String lastSeenDeviceId) |
| `MaxPageSize` | `int` | Required | Maximum page size. | int getMaxPageSize() | setMaxPageSize(int maxPageSize) |
| `DeviceList` | [`List<V2DeviceStatus>`](../../doc/models/v2-device-status.md) | Required | List of devices with id in IMEI. | List<V2DeviceStatus> getDeviceList() | setDeviceList(List<V2DeviceStatus> deviceList) |

## Example

```java
import com.verizon.thingspace.models.V2CampaignDevice;
import com.verizon.thingspace.models.V2DeviceStatus;
import java.util.Arrays;

V2CampaignDevice v2CampaignDevice = new V2CampaignDevice.Builder(
    true,
    1000,
    Arrays.asList(
        new V2DeviceStatus.Builder(
            "15-digit IMEI",
            "UpgradeSuccess"
        )
        .resultReason("DownloadInstallSucceeded")
        .build(),
        new V2DeviceStatus.Builder(
            "15-digit IMEI",
            "UpgradeSuccess"
        )
        .resultReason("DownloadInstallSucceeded")
        .build(),
        new V2DeviceStatus.Builder(
            "15-digit IMEI",
            "UpgradeSuccess"
        )
        .resultReason("DownloadInstallSucceeded")
        .build()
    )
)
.totalDevice(1148)
.lastSeenDeviceId("15-digit IMEI")
.build();
```

