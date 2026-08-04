
# Dto Last Reported Time Response

## Structure

`DtoLastReportedTimeResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Event` | [`ResourceEvent`](../../doc/models/resource-event.md) | Optional | - | ResourceEvent getEvent() | setEvent(ResourceEvent event) |
| `Timestamp` | `String` | Optional | - | String getTimestamp() | setTimestamp(String timestamp) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.DtoLastReportedTimeResponse;
import com.verizon.thingspace.models.ResourceEvent;

DtoLastReportedTimeResponse dtoLastReportedTimeResponse = new DtoLastReportedTimeResponse.Builder()
    .event(new ResourceEvent.Builder(
        DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"),
        "fieldid6",
        "foreignid8",
        DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"),
        "state4",
        "versionid2"
    )
    .accountclientid("accountclientid4")
    .callbackurl("callbackurl0")
    .description("description0")
    .deviceid("deviceid0")
    .errmsg("errmsg2")
    .build())
    .timestamp("timestamp4")
    .build();
```

