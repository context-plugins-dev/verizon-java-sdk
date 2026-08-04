
# V3 Change Campaign Dates Request

Campaign dates and time windows.

## Structure

`V3ChangeCampaignDatesRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `StartDate` | `LocalDate` | Required | Campaign start date. | LocalDate getStartDate() | setStartDate(LocalDate startDate) |
| `EndDate` | `LocalDate` | Required | Campaign end date. | LocalDate getEndDate() | setEndDate(LocalDate endDate) |
| `CampaignTimeWindowList` | [`List<V3TimeWindow>`](../../doc/models/v3-time-window.md) | Optional | List of allowed campaign time windows. | List<V3TimeWindow> getCampaignTimeWindowList() | setCampaignTimeWindowList(List<V3TimeWindow> campaignTimeWindowList) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.V3ChangeCampaignDatesRequest;
import com.verizon.thingspace.models.V3TimeWindow;
import java.util.Arrays;

V3ChangeCampaignDatesRequest v3ChangeCampaignDatesRequest = new V3ChangeCampaignDatesRequest.Builder(
    DateTimeHelper.fromSimpleDate("2022-02-23"),
    DateTimeHelper.fromSimpleDate("2022-02-24")
)
.campaignTimeWindowList(Arrays.asList(
        new V3TimeWindow.Builder(
            14,
            18
        )
        .build()
    ))
.build();
```

