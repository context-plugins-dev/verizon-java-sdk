
# V3 Add or Remove Device Result

Add or remove devices to existing upgrade information.

## Structure

`V3AddOrRemoveDeviceResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | Account identifier. | String getAccountName() | setAccountName(String accountName) |
| `CampaignId` | `String` | Required | Campaign identifier. | String getCampaignId() | setCampaignId(String campaignId) |
| `DeviceList` | [`List<V3DeviceListItem>`](../../doc/models/v3-device-list-item.md) | Required | Array of devices changed. | List<V3DeviceListItem> getDeviceList() | setDeviceList(List<V3DeviceListItem> deviceList) |

## Example

```java
import com.verizon.thingspace.models.V3AddOrRemoveDeviceResult;
import com.verizon.thingspace.models.V3DeviceListItem;
import java.util.Arrays;

V3AddOrRemoveDeviceResult v3AddOrRemoveDeviceResult = new V3AddOrRemoveDeviceResult.Builder(
    "0000123456-00001",
    "f858b8c4-2153-11ec-8c44-aeb16d1aa652",
    Arrays.asList(
        new V3DeviceListItem.Builder()
            .deviceId("15-digit IMEI")
            .status("AddDeviceSucceed")
            .reason("Device added Successfully")
            .build()
    )
)
.build();
```

