
# Location

Device location information.

## Structure

`Location`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Msid` | `String` | Optional | MDN. | String getMsid() | setMsid(String msid) |
| `Pd` | [`PositionData`](../../doc/models/position-data.md) | Optional | Position data. | PositionData getPd() | setPd(PositionData pd) |
| `Error` | [`PositionError`](../../doc/models/position-error.md) | Optional | Position error. | PositionError getError() | setError(PositionError error) |

## Example

```java
import com.verizon.thingspace.models.Location;
import com.verizon.thingspace.models.PositionData;
import com.verizon.thingspace.models.PositionError;

Location location = new Location.Builder()
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
    .build();
```

