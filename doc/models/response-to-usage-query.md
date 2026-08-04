
# Response to Usage Query

## Structure

`ResponseToUsageQuery`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Hasmoredata` | `Boolean` | Optional | - | Boolean getHasmoredata() | setHasmoredata(Boolean hasmoredata) |
| `DeviceId` | [`ReadySimDeviceId`](../../doc/models/ready-sim-device-id.md) | Optional | - | ReadySimDeviceId getDeviceId() | setDeviceId(ReadySimDeviceId deviceId) |
| `UsageHistory` | [`List<UsageHistory>`](../../doc/models/usage-history.md) | Optional | - | List<UsageHistory> getUsageHistory() | setUsageHistory(List<UsageHistory> usageHistory) |

## Example

```java
import com.verizon.thingspace.models.ReadySimDeviceId;
import com.verizon.thingspace.models.ResponseToUsageQuery;
import com.verizon.thingspace.models.UsageHistory;
import java.util.Arrays;

ResponseToUsageQuery responseToUsageQuery = new ResponseToUsageQuery.Builder()
    .hasmoredata(false)
    .deviceId(new ReadySimDeviceId.Builder()
        .kind("kind8")
        .id("id0")
        .build())
    .usageHistory(Arrays.asList(
        new UsageHistory.Builder()
            .bytesUsed(76)
            .serviceplan("serviceplan2")
            .smsUsed(176)
            .moSMS(230)
            .mtSMS(18)
            .build(),
        new UsageHistory.Builder()
            .bytesUsed(76)
            .serviceplan("serviceplan2")
            .smsUsed(176)
            .moSMS(230)
            .mtSMS(18)
            .build(),
        new UsageHistory.Builder()
            .bytesUsed(76)
            .serviceplan("serviceplan2")
            .smsUsed(176)
            .moSMS(230)
            .mtSMS(18)
            .build()
    ))
    .build();
```

