
# Get Trigger Response List

## Structure

`GetTriggerResponseList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Triggers` | [`List<GetTriggerResponse>`](../../doc/models/get-trigger-response.md) | Optional | **Constraints**: *Maximum Items*: `3` | List<GetTriggerResponse> getTriggers() | setTriggers(List<GetTriggerResponse> triggers) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.GetTriggerResponse;
import com.verizon.thingspace.models.GetTriggerResponseList;
import java.util.Arrays;

GetTriggerResponseList getTriggerResponseList = new GetTriggerResponseList.Builder()
    .triggers(Arrays.asList(
        new GetTriggerResponse.Builder()
            .accountName("accountName4")
            .comparator("comparator2")
            .createdAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .groupName("groupName0")
            .modifiedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .build()
    ))
    .build();
```

