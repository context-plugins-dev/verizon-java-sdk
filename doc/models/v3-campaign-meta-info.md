
# V3 Campaign Meta Info

Campaign and campaign details.

## Structure

`V3CampaignMetaInfo`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | Account identifier. | String getAccountName() | setAccountName(String accountName) |
| `Id` | `String` | Required | Campaign identifier. | String getId() | setId(String id) |
| `CampaignName` | `String` | Optional | Campaign name. | String getCampaignName() | setCampaignName(String campaignName) |
| `FirmwareName` | `String` | Optional | Firmware name. | String getFirmwareName() | setFirmwareName(String firmwareName) |
| `FirmwareFrom` | `String` | Optional | Old firmware version. | String getFirmwareFrom() | setFirmwareFrom(String firmwareFrom) |
| `FirmwareTo` | `String` | Optional | New software version. | String getFirmwareTo() | setFirmwareTo(String firmwareTo) |
| `Protocol` | [`CampaignMetaInfoProtocolEnum`](../../doc/models/campaign-meta-info-protocol-enum.md) | Optional | Firmware protocol. Valid values include: LWM2M, OMD-DM.<br><br>**Default**: `CampaignMetaInfoProtocolEnum.LW_M2M` | CampaignMetaInfoProtocolEnum getProtocol() | setProtocol(CampaignMetaInfoProtocolEnum protocol) |
| `Make` | `String` | Required | Device make. | String getMake() | setMake(String make) |
| `Model` | `String` | Required | Device model. | String getModel() | setModel(String model) |
| `StartDate` | `LocalDate` | Required | Campaign start date. | LocalDate getStartDate() | setStartDate(LocalDate startDate) |
| `EndDate` | `LocalDate` | Required | Campaign end date. | LocalDate getEndDate() | setEndDate(LocalDate endDate) |
| `CampaignTimeWindowList` | [`List<V3TimeWindow>`](../../doc/models/v3-time-window.md) | Optional | List of allowed campaign time windows. | List<V3TimeWindow> getCampaignTimeWindowList() | setCampaignTimeWindowList(List<V3TimeWindow> campaignTimeWindowList) |
| `Status` | `String` | Required | Firmware upgrade status. | String getStatus() | setStatus(String status) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.CampaignMetaInfoProtocolEnum;
import com.verizon.thingspace.models.V3CampaignMetaInfo;
import com.verizon.thingspace.models.V3TimeWindow;
import java.util.Arrays;

V3CampaignMetaInfo v3CampaignMetaInfo = new V3CampaignMetaInfo.Builder(
    "0000123456-00001",
    "60b5d639-ccdc-4db8-8824-069bd94c95bf",
    "Verizon",
    "Model-A",
    DateTimeHelper.fromSimpleDate("2020-08-21"),
    DateTimeHelper.fromSimpleDate("2020-08-22"),
    "CampaignEnded"
)
.campaignName("FOTA_Verizon_Upgrade")
.firmwareName("FOTA_Verizon_Model-A_02To03_HF")
.firmwareFrom("FOTA_Verizon_Model-A_00To01_HF")
.firmwareTo("FOTA_Verizon_Model-A_02To03_HF")
.protocol(CampaignMetaInfoProtocolEnum.LW_M2M)
.campaignTimeWindowList(Arrays.asList(
        new V3TimeWindow.Builder(
            20,
            21
        )
        .build()
    ))
.build();
```

