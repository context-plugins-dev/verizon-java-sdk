
# Sms Messages Response

## Structure

`SmsMessagesResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Messages` | [`List<SmsMessagesResponseMessages>`](../../doc/models/containers/sms-messages-response-messages.md) | Optional | This is List of a container for any-of cases.<br><br>**Constraints**: *Maximum Items*: `5` | List<SmsMessagesResponseMessages> getMessages() | setMessages(List<SmsMessagesResponseMessages> messages) |
| `HasMoreData` | `Boolean` | Optional | - | Boolean getHasMoreData() | setHasMoreData(Boolean hasMoreData) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.GIODeviceId;
import com.verizon.thingspace.models.GIOSmsMessage;
import com.verizon.thingspace.models.SmsMessagesResponse;
import com.verizon.thingspace.models.containers.SmsMessagesResponseMessages;
import java.util.Arrays;

SmsMessagesResponse smsMessagesResponse = new SmsMessagesResponse.Builder()
    .messages(Arrays.asList(
        SmsMessagesResponseMessages.fromGIOSmsMessage(
            new GIOSmsMessage.Builder()
                .deviceIds(Arrays.asList(
                    new GIODeviceId.Builder(
                        "kind8",
                        "id0"
                    )
                    .build()
                ))
                .message("message4")
                .timestamp(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .build()
        )
    ))
    .hasMoreData(false)
    .build();
```

