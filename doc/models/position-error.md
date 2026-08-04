
# Position Error

Position error.

## Structure

`PositionError`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Time` | `String` | Optional | Time location obtained. | String getTime() | setTime(String time) |
| `Utcoffset` | `String` | Optional | UTC offset of time. | String getUtcoffset() | setUtcoffset(String utcoffset) |
| `Type` | `String` | Optional | Error type returned from location server. | String getType() | setType(String type) |
| `Info` | `String` | Optional | Additional information about the error. | String getInfo() | setInfo(String info) |

## Example

```java
import com.verizon.thingspace.models.PositionError;

PositionError positionError = new PositionError.Builder()
    .time("20170525214342")
    .utcoffset("utcoffset6")
    .type("POSITION METHOD FAILURE")
    .info("Exception code=ABSENT SUBSCRIBER")
    .build();
```

