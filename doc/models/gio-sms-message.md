
# GIO Sms Message

## Structure

`GIOSmsMessage`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceIds` | [`List<GIODeviceId>`](../../doc/models/gio-device-id.md) | Optional | **Constraints**: *Maximum Items*: `100` | List<GIODeviceId> getDeviceIds() | setDeviceIds(List<GIODeviceId> deviceIds) |
| `Message` | `String` | Optional | **Constraints**: *Minimum Length*: `3`, *Maximum Length*: `120`, *Pattern*: `^[A-Za-z0-9 ]{3,120}$` | String getMessage() | setMessage(String message) |
| `Timestamp` | `LocalDateTime` | Optional | - | LocalDateTime getTimestamp() | setTimestamp(LocalDateTime timestamp) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.GIODeviceId;
import com.verizon.thingspace.models.GIOSmsMessage;
import java.util.Arrays;

GIOSmsMessage gIOSmsMessage = new GIOSmsMessage.Builder()
    .deviceIds(Arrays.asList(
        new GIODeviceId.Builder(
            "kind8",
            "id0"
        )
        .build(),
        new GIODeviceId.Builder(
            "kind8",
            "id0"
        )
        .build(),
        new GIODeviceId.Builder(
            "kind8",
            "id0"
        )
        .build()
    ))
    .message("a text message")
    .timestamp(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .build();
```

