
# V2 Change Campaign Dates Request

New dates and time windows.

## Structure

`V2ChangeCampaignDatesRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `StartDate` | `LocalDate` | Required | Campaign start date. | LocalDate getStartDate() | setStartDate(LocalDate startDate) |
| `EndDate` | `LocalDate` | Required | Campaign end date. | LocalDate getEndDate() | setEndDate(LocalDate endDate) |
| `DownloadAfterDate` | `LocalDate` | Optional | Specifies starting date client should download package. If null, client will download as soon as possible. | LocalDate getDownloadAfterDate() | setDownloadAfterDate(LocalDate downloadAfterDate) |
| `DownloadTimeWindowList` | [`List<V2TimeWindow>`](../../doc/models/v2-time-window.md) | Optional | List of allowed download time windows. Removing of existing windows is not allowed. | List<V2TimeWindow> getDownloadTimeWindowList() | setDownloadTimeWindowList(List<V2TimeWindow> downloadTimeWindowList) |
| `InstallAfterDate` | `LocalDate` | Optional | Client will install package after date. If null, client will install as soon as possible. | LocalDate getInstallAfterDate() | setInstallAfterDate(LocalDate installAfterDate) |
| `InstallTimeWindowList` | [`List<V2TimeWindow>`](../../doc/models/v2-time-window.md) | Optional | List of allowed install time windows. Removing of existing windows is not allowed. | List<V2TimeWindow> getInstallTimeWindowList() | setInstallTimeWindowList(List<V2TimeWindow> installTimeWindowList) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.V2ChangeCampaignDatesRequest;
import com.verizon.thingspace.models.V2TimeWindow;
import java.util.Arrays;

V2ChangeCampaignDatesRequest v2ChangeCampaignDatesRequest = new V2ChangeCampaignDatesRequest.Builder(
    DateTimeHelper.fromSimpleDate("2020-08-21"),
    DateTimeHelper.fromSimpleDate("2020-08-22")
)
.downloadAfterDate(DateTimeHelper.fromSimpleDate("2020-08-21"))
.downloadTimeWindowList(Arrays.asList(
        new V2TimeWindow.Builder(
            3,
            4
        )
        .build()
    ))
.installAfterDate(DateTimeHelper.fromSimpleDate("2020-08-21"))
.installTimeWindowList(Arrays.asList(
        new V2TimeWindow.Builder(
            5,
            6
        )
        .build()
    ))
.build();
```

