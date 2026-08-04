
# Firmware Package

Available firmware.

## Structure

`FirmwarePackage`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `FirmwareName` | `String` | Required | Firmware name. | String getFirmwareName() | setFirmwareName(String firmwareName) |
| `FirmwareFrom` | `String` | Required | Firmware from version. | String getFirmwareFrom() | setFirmwareFrom(String firmwareFrom) |
| `FirmwareTo` | `String` | Required | Firmware to version. | String getFirmwareTo() | setFirmwareTo(String firmwareTo) |
| `LaunchDate` | `LocalDateTime` | Required | Firmware launch date. | LocalDateTime getLaunchDate() | setLaunchDate(LocalDateTime launchDate) |
| `ReleaseNote` | `String` | Required | Firmware release note. | String getReleaseNote() | setReleaseNote(String releaseNote) |
| `Model` | `String` | Required | Firmware applicable device model. | String getModel() | setModel(String model) |
| `Make` | `String` | Required | Firmware applicable device make. | String getMake() | setMake(String make) |
| `Protocol` | [`CampaignMetaInfoProtocolEnum`](../../doc/models/campaign-meta-info-protocol-enum.md) | Required | Firmware protocol. Valid values include: LWM2M, OMD-DM.<br><br>**Default**: `CampaignMetaInfoProtocolEnum.LW_M2M` | CampaignMetaInfoProtocolEnum getProtocol() | setProtocol(CampaignMetaInfoProtocolEnum protocol) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.CampaignMetaInfoProtocolEnum;
import com.verizon.thingspace.models.FirmwarePackage;

FirmwarePackage firmwarePackage = new FirmwarePackage.Builder(
    "VerizonSmartCommunities_LCO-277C4N_BG96MAR04A04M1G_BG96MAR04A04M1G_BETA0130B",
    "BG96MAR04A04M1G",
    "BG96MAR04A04M1G_BETA0130B",
    DateTimeHelper.fromRfc8601DateTime("2012-04-23T18:25:43.511Z"),
    "",
    "LCO-277C4N",
    "Verizon Smart Communities",
    CampaignMetaInfoProtocolEnum.LW_M2M
)
.build();
```

