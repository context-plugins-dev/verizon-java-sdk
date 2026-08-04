
# Device Firmware Upgrade

Firmware upgrades information.

## Structure

`DeviceFirmwareUpgrade`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceId` | `String` | Required | Device identifier. | String getDeviceId() | setDeviceId(String deviceId) |
| `CampaignId` | `String` | Required | Campaign identifier. | String getCampaignId() | setCampaignId(String campaignId) |
| `AccountName` | `String` | Required | Account identifier. | String getAccountName() | setAccountName(String accountName) |
| `FirmwareName` | `String` | Optional | Firmware name. | String getFirmwareName() | setFirmwareName(String firmwareName) |
| `FirmwareFrom` | `String` | Optional | Old firmware version. | String getFirmwareFrom() | setFirmwareFrom(String firmwareFrom) |
| `FirmwareTo` | `String` | Optional | New firmware version. | String getFirmwareTo() | setFirmwareTo(String firmwareTo) |
| `StartDate` | `LocalDate` | Required | Firmware upgrade start date. | LocalDate getStartDate() | setStartDate(LocalDate startDate) |
| `Status` | `String` | Required | Firmware upgrade status. | String getStatus() | setStatus(String status) |
| `Reason` | `String` | Required | Software upgrade result reason. | String getReason() | setReason(String reason) |
| `ReportUpdatedTime` | `String` | Optional | Report updated time. | String getReportUpdatedTime() | setReportUpdatedTime(String reportUpdatedTime) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.DeviceFirmwareUpgrade;

DeviceFirmwareUpgrade deviceFirmwareUpgrade = new DeviceFirmwareUpgrade.Builder(
    "15-digit IMEI",
    "252d7ffc-7e35-11ec-931d-76f56843c393",
    "0000123456-00001",
    DateTimeHelper.fromSimpleDate("2022-01-25"),
    "UpgradeSuccess",
    "Upgrade completed successfully"
)
.firmwareName("SEQUANSCommunications_GM01Q_SR1.2.0.0-10657_SR1.2.0.0-10512")
.firmwareFrom("SR1.2.0.0-10657")
.firmwareTo("SR1.2.0.0-10512")
.reportUpdatedTime("2022-01-26 03:45:01.608 +0000 UTC")
.build();
```

