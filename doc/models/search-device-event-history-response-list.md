
# Search Device Event History Response List

A success response includes an array of all matching events.

## Structure

`SearchDeviceEventHistoryResponseList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SearchDeviceEventHistory` | [`List<SearchDeviceResponse>`](../../doc/models/search-device-response.md) | Optional | **Constraints**: *Maximum Items*: `100` | List<SearchDeviceResponse> getSearchDeviceEventHistory() | setSearchDeviceEventHistory(List<SearchDeviceResponse> searchDeviceEventHistory) |

## Example

```java
import com.verizon.thingspace.models.Fields2;
import com.verizon.thingspace.models.SearchDeviceEventHistoryResponseList;
import com.verizon.thingspace.models.SearchDeviceResponse;
import java.util.Arrays;

SearchDeviceEventHistoryResponseList searchDeviceEventHistoryResponseList = new SearchDeviceEventHistoryResponseList.Builder()
    .searchDeviceEventHistory(Arrays.asList(
        new SearchDeviceResponse.Builder()
            .action("action4")
            .createdon("createdon4")
            .deviceid("deviceid8")
            .fields(new Fields2.Builder()
                .temperature("temperature0")
                .build())
            .id("id8")
            .build(),
        new SearchDeviceResponse.Builder()
            .action("action4")
            .createdon("createdon4")
            .deviceid("deviceid8")
            .fields(new Fields2.Builder()
                .temperature("temperature0")
                .build())
            .id("id8")
            .build(),
        new SearchDeviceResponse.Builder()
            .action("action4")
            .createdon("createdon4")
            .deviceid("deviceid8")
            .fields(new Fields2.Builder()
                .temperature("temperature0")
                .build())
            .id("id8")
            .build()
    ))
    .build();
```

