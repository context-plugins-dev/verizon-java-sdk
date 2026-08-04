
# Connection History Result

Response containing the connection history. It is a list of Network Connection Events for a device.

## Structure

`ConnectionHistoryResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ConnectionHistory` | [`List<ConnectionEvent>`](../../doc/models/connection-event.md) | Optional | Device connection events, sorted by the occurredAt timestamp, oldest first. | List<ConnectionEvent> getConnectionHistory() | setConnectionHistory(List<ConnectionEvent> connectionHistory) |
| `HasMoreData` | `Boolean` | Optional | False for a status 200 response.True for a status 202 response, indicating that there is more data to be retrieved. Send another request, adjusting the earliest value in the request based on the occuredAt value for the last device in the current response. | Boolean getHasMoreData() | setHasMoreData(Boolean hasMoreData) |

## Example

```java
import com.verizon.thingspace.models.ConnectionEvent;
import com.verizon.thingspace.models.ConnectionHistoryResult;
import com.verizon.thingspace.models.CustomFields;
import java.util.Arrays;

ConnectionHistoryResult connectionHistoryResult = new ConnectionHistoryResult.Builder()
    .connectionHistory(Arrays.asList(
        new ConnectionEvent.Builder()
            .connectionEventAttributes(Arrays.asList(
                new CustomFields.Builder(
                    "BytesUsed",
                    "0"
                )
                .build(),
                new CustomFields.Builder(
                    "Event",
                    "Start"
                )
                .build()
            ))
            .extendedAttributes(Arrays.asList(

            ))
            .occurredAt("2015-12-17T14:12:36-05:00")
            .build(),
        new ConnectionEvent.Builder()
            .connectionEventAttributes(Arrays.asList(
                new CustomFields.Builder(
                    "BytesUsed",
                    "419863234"
                )
                .build(),
                new CustomFields.Builder(
                    "Event",
                    "Stop"
                )
                .build(),
                new CustomFields.Builder(
                    "Msisdn",
                    "15086303371"
                )
                .build()
            ))
            .extendedAttributes(Arrays.asList(

            ))
            .occurredAt("2015-12-19T01:20:00-05:00")
            .build()
    ))
    .hasMoreData(false)
    .build();
```

