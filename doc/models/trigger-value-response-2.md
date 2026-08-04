
# Trigger Value Response 2

## Structure

`TriggerValueResponse2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Triggers` | [`List<TriggervalueChunk2>`](../../doc/models/containers/triggervalue-chunk-2.md) | Optional | - | List<TriggervalueChunk2> getTriggers() | setTriggers(List<TriggervalueChunk2> triggers) |

## Example

```java
import com.verizon.thingspace.models.TriggerValueResponse2;
import com.verizon.thingspace.models.Triggervalues2;
import com.verizon.thingspace.models.containers.TriggervalueChunk2;
import java.util.Arrays;

TriggerValueResponse2 triggerValueResponse2 = new TriggerValueResponse2.Builder()
    .triggers(Arrays.asList(
        TriggervalueChunk2.fromTriggervalues2(
            new Triggervalues2.Builder()
                .triggerId("triggerId8")
                .triggerName("triggerName6")
                .accountName("accountName2")
                .organizationName("organizationName0")
                .triggerCategory("triggerCategory0")
                .build()
        ),
        TriggervalueChunk2.fromTriggervalues2(
            new Triggervalues2.Builder()
                .triggerId("triggerId8")
                .triggerName("triggerName6")
                .accountName("accountName2")
                .organizationName("organizationName0")
                .triggerCategory("triggerCategory0")
                .build()
        )
    ))
    .build();
```

