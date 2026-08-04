
# Firmware Campaign

Firmware upgrade information.

## Structure

`FirmwareCampaign`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Upgrade identifier. | String getId() | setId(String id) |
| `AccountName` | `String` | Required | Account identifier. | String getAccountName() | setAccountName(String accountName) |
| `CampaignName` | `String` | Optional | Campaign name. | String getCampaignName() | setCampaignName(String campaignName) |
| `FirmwareName` | `String` | Optional | Firmware name (for firmware upgrade only). | String getFirmwareName() | setFirmwareName(String firmwareName) |
| `FirmwareFrom` | `String` | Required | Old firmware version (for firmware upgrade only). | String getFirmwareFrom() | setFirmwareFrom(String firmwareFrom) |
| `FirmwareTo` | `String` | Required | New firmware version (for firmware upgrade only). | String getFirmwareTo() | setFirmwareTo(String firmwareTo) |
| `Protocol` | `String` | Required | Available values: LWM2M.<br><br>**Default**: `"LWM2M"` | String getProtocol() | setProtocol(String protocol) |
| `Make` | `String` | Required | - | String getMake() | setMake(String make) |
| `Model` | `String` | Required | - | String getModel() | setModel(String model) |
| `StartDate` | `LocalDate` | Required | Campaign start date. | LocalDate getStartDate() | setStartDate(LocalDate startDate) |
| `EndDate` | `LocalDate` | Required | Campaign end date. | LocalDate getEndDate() | setEndDate(LocalDate endDate) |
| `CampaignTimeWindowList` | [`List<V3TimeWindow>`](../../doc/models/v3-time-window.md) | Optional | List of allowed campaign time windows. | List<V3TimeWindow> getCampaignTimeWindowList() | setCampaignTimeWindowList(List<V3TimeWindow> campaignTimeWindowList) |
| `Status` | `String` | Required | Campaign status. | String getStatus() | setStatus(String status) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.FirmwareCampaign;
import com.verizon.thingspace.models.V3TimeWindow;
import java.util.Arrays;

FirmwareCampaign firmwareCampaign = new FirmwareCampaign.Builder(
    "f858b8c4-2153-11ec-8c44-aeb16d1aa652",
    "0000123456-00001",
    "SR1.2.0.0-10512",
    "SR1.2.0.0-10657",
    "LWM2M",
    "SEQUANS Communications",
    "GM01Q",
    DateTimeHelper.fromSimpleDate("2021-09-29"),
    DateTimeHelper.fromSimpleDate("2021-10-01"),
    "CampaignRequestPending"
)
.campaignName("Smart FOTA - test 4")
.firmwareName("SEQUANSCommunications_GM01Q_SR1.2.0.0-10512_SR1.2.0.0-10657")
.campaignTimeWindowList(Arrays.asList(
        new V3TimeWindow.Builder(
            18,
            22
        )
        .build()
    ))
.build();
```

