
# Trigger Value Response

## Structure

`TriggerValueResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Triggers` | [`List<TriggervalueChunk>`](../../doc/models/containers/triggervalue-chunk.md) | Optional | - | List<TriggervalueChunk> getTriggers() | setTriggers(List<TriggervalueChunk> triggers) |

## Example

```java
import com.verizon.thingspace.models.TriggerValueResponse;
import com.verizon.thingspace.models.Triggervalues;
import com.verizon.thingspace.models.containers.TriggervalueChunk;
import java.util.Arrays;

TriggerValueResponse triggerValueResponse = new TriggerValueResponse.Builder()
    .triggers(Arrays.asList(
        TriggervalueChunk.fromTriggervalues(
            new Triggervalues.Builder()
                .triggerId("triggerId4")
                .triggerName("triggerName2")
                .accountName("accountName8")
                .organizationName("organizationName6")
                .triggerCategory("triggerCategory6")
                .build()
        ),
        TriggervalueChunk.fromTriggervalues(
            new Triggervalues.Builder()
                .triggerId("triggerId4")
                .triggerName("triggerName2")
                .accountName("accountName8")
                .organizationName("organizationName6")
                .triggerCategory("triggerCategory6")
                .build()
        )
    ))
    .build();
```

