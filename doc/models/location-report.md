
# Location Report

Location information for up to 1,000 devices.

## Structure

`LocationReport`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DevLocationList` | [`List<Location>`](../../doc/models/location.md) | Optional | Device location information. | List<Location> getDevLocationList() | setDevLocationList(List<Location> devLocationList) |
| `HasMoreData` | `Boolean` | Optional | True if there are more device locations to retrieve. | Boolean getHasMoreData() | setHasMoreData(Boolean hasMoreData) |
| `StartIndex` | `String` | Optional | The zero-based number of the first record to return. Set startIndex=0 for the first request. If there are more than 1,000 devices to be returned (hasMoreData=true), set startIndex=1000 for the second request, 2000 for the third request, etc. | String getStartIndex() | setStartIndex(String startIndex) |
| `TotalCount` | `Integer` | Optional | The total number of devices in the original request and in the report. | Integer getTotalCount() | setTotalCount(Integer totalCount) |
| `Txid` | `String` | Optional | The transaction ID of the report. | String getTxid() | setTxid(String txid) |

## Example

```java
import com.verizon.thingspace.models.Location;
import com.verizon.thingspace.models.LocationReport;
import com.verizon.thingspace.models.PositionData;
import com.verizon.thingspace.models.PositionError;
import java.util.Arrays;

LocationReport locationReport = new LocationReport.Builder()
    .devLocationList(Arrays.asList(
        new Location.Builder()
            .msid("7892345678")
            .pd(new PositionData.Builder()
                .time("20170520004421")
                .utcoffset("utcoffset2")
                .x("33.45324")
                .y("-84.59621")
                .radius("5571")
                .qos(false)
                .build())
            .error(new PositionError.Builder()
                .time("time4")
                .utcoffset("utcoffset4")
                .type("type6")
                .info("info4")
                .build())
            .build(),
        new Location.Builder()
            .msid("8583239709")
            .pd(new PositionData.Builder()
                .time("20170525214342")
                .utcoffset("utcoffset2")
                .x("38.8408694")
                .y("-105.0422583")
                .radius("3866")
                .qos(false)
                .build())
            .error(new PositionError.Builder()
                .time("time4")
                .utcoffset("utcoffset4")
                .type("type6")
                .info("info4")
                .build())
            .build(),
        new Location.Builder()
            .msid("7897654321")
            .pd(new PositionData.Builder()
                .time("time2")
                .utcoffset("utcoffset2")
                .x("x8")
                .y("y6")
                .radius("radius0")
                .build())
            .error(new PositionError.Builder()
                .time("20170525214342")
                .utcoffset("utcoffset4")
                .type("POSITION METHOD FAILURE")
                .info("Exception code=ABSENT SUBSCRIBER")
                .build())
            .build()
    ))
    .hasMoreData(false)
    .startIndex("0")
    .totalCount(3)
    .txid("2017-12-11Te8b47da2-eeee-ffff-gggg-61815e1e97e9")
    .build();
```

