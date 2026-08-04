
# History Search Request

Used to filter data by time period or number of devices.

## Structure

`HistorySearchRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Filter` | [`HistorySearchFilter`](../../doc/models/history-search-filter.md) | Required | The selected device and attributes for which a request should retrieve data. | HistorySearchFilter getFilter() | setFilter(HistorySearchFilter filter) |
| `LimitNumber` | `Integer` | Optional | The maximum number of historical attributes to include in the response. If the request matches more than this number of attributes, the response will contain an X-Next value in the header that can be used as the page value in the next request to retrieve the next page of events. | Integer getLimitNumber() | setLimitNumber(Integer limitNumber) |
| `LimitTime` | [`HistorySearchLimitTime`](../../doc/models/history-search-limit-time.md) | Optional | The time period for which a request should retrieve data, beginning with the limitTime.startOn and proceeding with the limitTime.duration. | HistorySearchLimitTime getLimitTime() | setLimitTime(HistorySearchLimitTime limitTime) |
| `Page` | `String` | Optional | Page number for pagination purposes. | String getPage() | setPage(String page) |

## Example

```java
import com.verizon.thingspace.models.Device;
import com.verizon.thingspace.models.HistorySearchFilter;
import com.verizon.thingspace.models.HistorySearchRequest;

HistorySearchRequest historySearchRequest = new HistorySearchRequest.Builder(
    new HistorySearchFilter.Builder(
        "0000123456-00001",
        new Device.Builder(
            "15-digit IMEI",
            "IMEI"
        )
        .build()
    )
    .attributes(null)
    .build()
)
.limitNumber(122)
.limitTime(null)
.page("$page2")
.build();
```

