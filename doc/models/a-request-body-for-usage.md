
# A Request Body for Usage

## Structure

`ARequestBodyForUsage`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceId` | [`List<ReadySimDeviceId>`](../../doc/models/ready-sim-device-id.md) | Optional | - | List<ReadySimDeviceId> getDeviceId() | setDeviceId(List<ReadySimDeviceId> deviceId) |
| `StartTime` | `LocalDateTime` | Optional | - | LocalDateTime getStartTime() | setStartTime(LocalDateTime startTime) |
| `EndTime` | `LocalDateTime` | Optional | - | LocalDateTime getEndTime() | setEndTime(LocalDateTime endTime) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.ARequestBodyForUsage;
import com.verizon.thingspace.models.ReadySimDeviceId;
import java.util.Arrays;

ARequestBodyForUsage aRequestBodyForUsage = new ARequestBodyForUsage.Builder()
    .deviceId(Arrays.asList(
        new ReadySimDeviceId.Builder()
            .kind("kind8")
            .id("id0")
            .build()
    ))
    .startTime(DateTimeHelper.fromRfc8601DateTime("2021-08-15T00:00:00Z"))
    .endTime(DateTimeHelper.fromRfc8601DateTime("2021-08-16T00:00:00Z"))
    .build();
```

