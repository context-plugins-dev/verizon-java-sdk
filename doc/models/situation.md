
# Situation

This represents the situation container describing the event and the reliability of the detection source.

## Structure

`Situation`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `InformationQuality` | `int` | Required | The quality or reliability level of the information provided by the ITS-S application of the originating ITS-S.<br><br>**Constraints**: `>= 0`, `<= 7` | int getInformationQuality() | setInformationQuality(int informationQuality) |
| `EventType` | [`EventType`](../../doc/models/event-type.md) | Required | The type of event including direct and sub cause. | EventType getEventType() | setEventType(EventType eventType) |

## Example

```java
import com.verizon.thingspace.models.EventType;
import com.verizon.thingspace.models.Situation;
import com.verizon.thingspace.models.TrafficConditionCauseCode;
import com.verizon.thingspace.models.containers.CauseCodeChoice;

Situation situation = new Situation.Builder(
    7,
    new EventType.Builder()
        .ccAndScc(CauseCodeChoice.fromTrafficConditionCauseCode(
            new TrafficConditionCauseCode.Builder(
                26
            )
            .build()
        ))
        .build()
)
.build();
```

