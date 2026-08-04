
# Campaign Firmware Upgrade

Firmware upgrade for devices.

## Structure

`CampaignFirmwareUpgrade`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CampaignName` | `String` | Optional | Campaign name. | String getCampaignName() | setCampaignName(String campaignName) |
| `FirmwareName` | `String` | Required | Firmware name to upgrade to. | String getFirmwareName() | setFirmwareName(String firmwareName) |
| `FirmwareFrom` | `String` | Required | Old firmware version. | String getFirmwareFrom() | setFirmwareFrom(String firmwareFrom) |
| `FirmwareTo` | `String` | Required | New firmware version. | String getFirmwareTo() | setFirmwareTo(String firmwareTo) |
| `Protocol` | `String` | Required | Valid values include: LWM2M, OMA and HTTP.<br><br>**Default**: `"LWM2M"` | String getProtocol() | setProtocol(String protocol) |
| `StartDate` | `LocalDate` | Required | Campaign start date. | LocalDate getStartDate() | setStartDate(LocalDate startDate) |
| `EndDate` | `LocalDate` | Required | Campaign end date. | LocalDate getEndDate() | setEndDate(LocalDate endDate) |
| `CampaignTimeWindowList` | [`List<V3TimeWindow>`](../../doc/models/v3-time-window.md) | Optional | List of allowed campaign time windows. | List<V3TimeWindow> getCampaignTimeWindowList() | setCampaignTimeWindowList(List<V3TimeWindow> campaignTimeWindowList) |
| `DeviceList` | `List<String>` | Required | Device IMEI list. | List<String> getDeviceList() | setDeviceList(List<String> deviceList) |
| `AutoAssignLicenseFlag` | `boolean` | Required | This flag, when set to true, will assign a FOTA license automatically if the device does not have one already. | boolean getAutoAssignLicenseFlag() | setAutoAssignLicenseFlag(boolean autoAssignLicenseFlag) |
| `AutoAddDevicesFlag` | `boolean` | Required | this flag, when set to true, will automatically add a device of the same make and model to a campaign. | boolean getAutoAddDevicesFlag() | setAutoAddDevicesFlag(boolean autoAddDevicesFlag) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.CampaignFirmwareUpgrade;
import com.verizon.thingspace.models.V3TimeWindow;
import java.util.Arrays;

CampaignFirmwareUpgrade campaignFirmwareUpgrade = new CampaignFirmwareUpgrade.Builder(
    "SEQUANSCommunications_GM01Q_SR1.2.0.0-10512_SR1.2.0.0-10657",
    "SR1.2.0.0-10512",
    "SR1.2.0.0-10657",
    "LWM2M",
    DateTimeHelper.fromSimpleDate("2021-09-29"),
    DateTimeHelper.fromSimpleDate("2021-10-01"),
    Arrays.asList(
        "15-digit IMEI"
    ),
    false,
    false
)
.campaignName("Smart FOTA - test 4")
.campaignTimeWindowList(Arrays.asList(
        new V3TimeWindow.Builder(
            18,
            22
        )
        .build()
    ))
.build();
```

