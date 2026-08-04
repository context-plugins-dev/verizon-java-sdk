
# SMS Messages Query Result

Response to SMS messages sent by all M2M devices associated with a billing account.

## Structure

`SMSMessagesQueryResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `HasMoreData` | `Boolean` | Optional | False for a status 200 response.True for a status 202 response, indicating that there is more data to be retrieved. | Boolean getHasMoreData() | setHasMoreData(Boolean hasMoreData) |
| `Messages` | [`List<SMSMessage>`](../../doc/models/sms-message.md) | Optional | An array of up to 100 SMS messages that were sent by devices in the account. | List<SMSMessage> getMessages() | setMessages(List<SMSMessage> messages) |

## Example

```java
import com.verizon.thingspace.models.DeviceId;
import com.verizon.thingspace.models.SMSMessage;
import com.verizon.thingspace.models.SMSMessagesQueryResult;
import java.util.Arrays;

SMSMessagesQueryResult sMSMessagesQueryResult = new SMSMessagesQueryResult.Builder()
    .hasMoreData(false)
    .messages(Arrays.asList(
        new SMSMessage.Builder()
            .deviceIds(Arrays.asList(
                new DeviceId.Builder(
                    "09623489171",
                    "esn"
                )
                .build()
            ))
            .message("testmessage1")
            .timestamp("2016-01-01T12:29:49-08:00")
            .build(),
        new SMSMessage.Builder()
            .deviceIds(Arrays.asList(
                new DeviceId.Builder(
                    "09623489171",
                    "esn"
                )
                .build()
            ))
            .message("testmessage2")
            .timestamp("2016-01-01T12:31:02-08:00")
            .build()
    ))
    .build();
```

