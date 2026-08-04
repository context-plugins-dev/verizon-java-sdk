
# Campaign Software Upgrade

Software upgrade information.

## Structure

`CampaignSoftwareUpgrade`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CampaignName` | `String` | Optional | Campaign name. | String getCampaignName() | setCampaignName(String campaignName) |
| `SoftwareName` | `String` | Required | Software name to upgrade to. | String getSoftwareName() | setSoftwareName(String softwareName) |
| `SoftwareFrom` | `String` | Required | Old software name. | String getSoftwareFrom() | setSoftwareFrom(String softwareFrom) |
| `SoftwareTo` | `String` | Required | New software name. | String getSoftwareTo() | setSoftwareTo(String softwareTo) |
| `DistributionType` | `String` | Required | OMA or HTTP. | String getDistributionType() | setDistributionType(String distributionType) |
| `StartDate` | `LocalDate` | Required | Campaign start date. | LocalDate getStartDate() | setStartDate(LocalDate startDate) |
| `EndDate` | `LocalDate` | Required | Campaign end date. | LocalDate getEndDate() | setEndDate(LocalDate endDate) |
| `DownloadAfterDate` | `LocalDate` | Optional | Specifies starting date client should download package. If null, client will download as soon as possible. | LocalDate getDownloadAfterDate() | setDownloadAfterDate(LocalDate downloadAfterDate) |
| `DownloadTimeWindowList` | [`List<V2TimeWindow>`](../../doc/models/v2-time-window.md) | Optional | List of allowed download time windows. | List<V2TimeWindow> getDownloadTimeWindowList() | setDownloadTimeWindowList(List<V2TimeWindow> downloadTimeWindowList) |
| `InstallAfterDate` | `LocalDate` | Optional | Client will install package after date. If null, client will install as soon as possible. | LocalDate getInstallAfterDate() | setInstallAfterDate(LocalDate installAfterDate) |
| `InstallTimeWindowList` | [`List<V2TimeWindow>`](../../doc/models/v2-time-window.md) | Optional | List of allowed install time windows. | List<V2TimeWindow> getInstallTimeWindowList() | setInstallTimeWindowList(List<V2TimeWindow> installTimeWindowList) |
| `DeviceList` | `List<String>` | Required | Device IMEI list. | List<String> getDeviceList() | setDeviceList(List<String> deviceList) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.CampaignSoftwareUpgrade;
import com.verizon.thingspace.models.V2TimeWindow;
import java.util.Arrays;

CampaignSoftwareUpgrade campaignSoftwareUpgrade = new CampaignSoftwareUpgrade.Builder(
    "FOTA_Verizon_Model-A_02To03_HF",
    "FOTA_Verizon_Model-A_00To01_HF",
    "FOTA_Verizon_Model-A_02To03_HF",
    "HTTP",
    DateTimeHelper.fromSimpleDate("2020-08-21"),
    DateTimeHelper.fromSimpleDate("2020-08-22"),
    Arrays.asList(
        "990013907835573",
        "990013907884259"
    )
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

