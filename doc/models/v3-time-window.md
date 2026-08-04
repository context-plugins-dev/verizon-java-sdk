
# V3 Time Window

Time window.

## Structure

`V3TimeWindow`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `StartTime` | `int` | Required | Start hour in range [0..23], current hour >= startTime. | int getStartTime() | setStartTime(int startTime) |
| `EndTime` | `int` | Required | End hour in range [1..24], current hour < endTime. | int getEndTime() | setEndTime(int endTime) |

## Example

```java
import com.verizon.thingspace.models.V3TimeWindow;

V3TimeWindow v3TimeWindow = new V3TimeWindow.Builder(
    18,
    22
)
.build();
```

