
# Search Sensor History Response List

A success response includes an array of all matching events.

## Structure

`SearchSensorHistoryResponseList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SearchSensorHistory` | [`List<SearchDeviceResponse>`](../../doc/models/search-device-response.md) | Optional | **Constraints**: *Maximum Items*: `100` | List<SearchDeviceResponse> getSearchSensorHistory() | setSearchSensorHistory(List<SearchDeviceResponse> searchSensorHistory) |

## Example

```java
import com.verizon.thingspace.models.Fields2;
import com.verizon.thingspace.models.SearchDeviceResponse;
import com.verizon.thingspace.models.SearchSensorHistoryResponseList;
import java.util.Arrays;

SearchSensorHistoryResponseList searchSensorHistoryResponseList = new SearchSensorHistoryResponseList.Builder()
    .searchSensorHistory(Arrays.asList(
        new SearchDeviceResponse.Builder()
            .action("action6")
            .createdon("createdon6")
            .deviceid("deviceid6")
            .fields(new Fields2.Builder()
                .temperature("temperature0")
                .build())
            .id("id6")
            .build(),
        new SearchDeviceResponse.Builder()
            .action("action6")
            .createdon("createdon6")
            .deviceid("deviceid6")
            .fields(new Fields2.Builder()
                .temperature("temperature0")
                .build())
            .id("id6")
            .build(),
        new SearchDeviceResponse.Builder()
            .action("action6")
            .createdon("createdon6")
            .deviceid("deviceid6")
            .fields(new Fields2.Builder()
                .temperature("temperature0")
                .build())
            .id("id6")
            .build()
    ))
    .build();
```

