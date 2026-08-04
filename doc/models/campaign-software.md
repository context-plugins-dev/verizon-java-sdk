
# Campaign Software

Software upgrade information.

## Structure

`CampaignSoftware`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Upgrade identifier. | String getId() | setId(String id) |
| `AccountName` | `String` | Required | Account identifier. | String getAccountName() | setAccountName(String accountName) |
| `CampaignName` | `String` | Optional | Campaign name. | String getCampaignName() | setCampaignName(String campaignName) |
| `SoftwareName` | `String` | Required | Software name. | String getSoftwareName() | setSoftwareName(String softwareName) |
| `DistributionType` | `String` | Required | LWM2M, OMD-DM or HTTP. | String getDistributionType() | setDistributionType(String distributionType) |
| `Make` | `String` | Required | Applicable make. | String getMake() | setMake(String make) |
| `Model` | `String` | Required | Applicable model. | String getModel() | setModel(String model) |
| `SoftwareFrom` | `String` | Required | Old software name. | String getSoftwareFrom() | setSoftwareFrom(String softwareFrom) |
| `SoftwareTo` | `String` | Required | New software name. | String getSoftwareTo() | setSoftwareTo(String softwareTo) |
| `StartDate` | `LocalDate` | Required | Campaign start date. | LocalDate getStartDate() | setStartDate(LocalDate startDate) |
| `EndDate` | `LocalDate` | Required | Campaign end date. | LocalDate getEndDate() | setEndDate(LocalDate endDate) |
| `DownloadAfterDate` | `LocalDate` | Optional | Specifies starting date client should download package. If null, client will download as soon as possible. | LocalDate getDownloadAfterDate() | setDownloadAfterDate(LocalDate downloadAfterDate) |
| `DownloadTimeWindowList` | [`List<V2TimeWindow>`](../../doc/models/v2-time-window.md) | Optional | List of allowed download time windows. | List<V2TimeWindow> getDownloadTimeWindowList() | setDownloadTimeWindowList(List<V2TimeWindow> downloadTimeWindowList) |
| `InstallAfterDate` | `LocalDate` | Optional | Client will install package after date. If null, client will install as soon as possible. | LocalDate getInstallAfterDate() | setInstallAfterDate(LocalDate installAfterDate) |
| `InstallTimeWindowList` | [`List<V2TimeWindow>`](../../doc/models/v2-time-window.md) | Optional | List of allowed install time windows. | List<V2TimeWindow> getInstallTimeWindowList() | setInstallTimeWindowList(List<V2TimeWindow> installTimeWindowList) |
| `Status` | `String` | Required | Software upgrade status. | String getStatus() | setStatus(String status) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.CampaignSoftware;
import com.verizon.thingspace.models.V2TimeWindow;
import java.util.Arrays;

CampaignSoftware campaignSoftware = new CampaignSoftware.Builder(
    "60b5d639-ccdc-4db8-8824-069bd94c95bf",
    "0402196254-00001",
    "FOTA_Verizon_Model-A_02To03_HF",
    "HTTP",
    "Verizon",
    "Model-A",
    "FOTA_Verizon_Model-A_00To01_HF",
    "FOTA_Verizon_Model-A_02To03_HF",
    DateTimeHelper.fromSimpleDate("2020-08-21"),
    DateTimeHelper.fromSimpleDate("2020-08-22"),
    "CampaignRequestPending"
)
.campaignName("FOTA_Verizon_Upgrade")
.downloadAfterDate(DateTimeHelper.fromSimpleDate("2020-08-21"))
.downloadTimeWindowList(Arrays.asList(
        new V2TimeWindow.Builder(
            20,
            21
        )
        .build()
    ))
.installAfterDate(DateTimeHelper.fromSimpleDate("2020-08-21"))
.installTimeWindowList(Arrays.asList(
        new V2TimeWindow.Builder(
            22,
            23
        )
        .build()
    ))
.build();
```

