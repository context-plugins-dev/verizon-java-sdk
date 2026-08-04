
# Distribution Schedule

The distribution schedule parameters for broadcast messages.

## Structure

`DistributionSchedule`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `RepeatPeriod` | `int` | Required | The period (in seconds) that the message needs to be repeatedly send out.<br><br>**Constraints**: `>= 5`, `<= 3600` | int getRepeatPeriod() | setRepeatPeriod(int repeatPeriod) |
| `Duration` | `int` | Required | The amount of time (in minutes) while the messages needs to be sent out.<br><br>**Constraints**: `>= 1`, `<= 32000` | int getDuration() | setDuration(int duration) |
| `StartTime` | `LocalDateTime` | Optional | The time (in UTC) when the message transmission should be started. | LocalDateTime getStartTime() | setStartTime(LocalDateTime startTime) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.DistributionSchedule;

DistributionSchedule distributionSchedule = new DistributionSchedule.Builder(
    90,
    88
)
.startTime(DateTimeHelper.fromRfc8601DateTime("2042-07-21T17:32:28Z"))
.build();
```

