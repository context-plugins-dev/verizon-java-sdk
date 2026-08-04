
# SMS Event History Request

## Structure

`SMSEventHistoryRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceId` | [`GIODeviceId`](../../doc/models/gio-device-id.md) | Required | - | GIODeviceId getDeviceId() | setDeviceId(GIODeviceId deviceId) |
| `Earliest` | `LocalDateTime` | Optional | - | LocalDateTime getEarliest() | setEarliest(LocalDateTime earliest) |
| `Latest` | `LocalDateTime` | Optional | - | LocalDateTime getLatest() | setLatest(LocalDateTime latest) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.GIODeviceId;
import com.verizon.thingspace.models.SMSEventHistoryRequest;

SMSEventHistoryRequest sMSEventHistoryRequest = new SMSEventHistoryRequest.Builder(
    new GIODeviceId.Builder(
        "eid",
        "12345678901234567890123456789012"
    )
    .build()
)
.earliest(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
.latest(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
.build();
```

