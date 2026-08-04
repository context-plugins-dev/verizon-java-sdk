
# Daily Usage Item

Contains only dates when device had sessions.

## Structure

`DailyUsageItem`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `StartTime` | `String` | Optional | Start date of session. ISO 8601 format. | String getStartTime() | setStartTime(String startTime) |
| `EndTime` | `String` | Optional | End date of session. ISO 8601 format. | String getEndTime() | setEndTime(String endTime) |
| `NumBytes` | `Integer` | Optional | Amount of data transferred, measured in Bytes. | Integer getNumBytes() | setNumBytes(Integer numBytes) |

## Example

```java
import com.verizon.thingspace.models.DailyUsageItem;

DailyUsageItem dailyUsageItem = new DailyUsageItem.Builder()
    .startTime("startTime4")
    .endTime("endTime2")
    .numBytes(138)
    .build();
```

