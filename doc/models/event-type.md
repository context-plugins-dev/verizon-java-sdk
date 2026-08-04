
# Event Type

The type of event including direct and sub cause.

## Structure

`EventType`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CcAndScc` | [`CauseCodeChoice`](../../doc/models/containers/cause-code-choice.md) | Optional | The main cause of a detected event. Each entry is of a different type and represents the sub cause code. | CauseCodeChoice getCcAndScc() | setCcAndScc(CauseCodeChoice ccAndScc) |

## Example

```java
import com.verizon.thingspace.models.EventType;
import com.verizon.thingspace.models.TrafficConditionCauseCode;
import com.verizon.thingspace.models.containers.CauseCodeChoice;

EventType eventType = new EventType.Builder()
    .ccAndScc(CauseCodeChoice.fromTrafficConditionCauseCode(
        new TrafficConditionCauseCode.Builder(
            26
        )
        .build()
    ))
    .build();
```

