
# Request Body for Usage

## Structure

`RequestBodyForUsage`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountId` | `String` | Optional | - | String getAccountId() | setAccountId(String accountId) |
| `DeviceId` | [`List<ReadySimDeviceId>`](../../doc/models/ready-sim-device-id.md) | Optional | - | List<ReadySimDeviceId> getDeviceId() | setDeviceId(List<ReadySimDeviceId> deviceId) |
| `StartTime` | `LocalDateTime` | Optional | - | LocalDateTime getStartTime() | setStartTime(LocalDateTime startTime) |
| `EndTime` | `LocalDateTime` | Optional | - | LocalDateTime getEndTime() | setEndTime(LocalDateTime endTime) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.ReadySimDeviceId;
import com.verizon.thingspace.models.RequestBodyForUsage;
import java.util.Arrays;

RequestBodyForUsage requestBodyForUsage = new RequestBodyForUsage.Builder()
    .accountId("0000123456-000001")
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

