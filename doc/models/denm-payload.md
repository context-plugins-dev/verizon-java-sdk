
# Denm Payload

The payload of the DENM PDU.

## Structure

`DenmPayload`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Management` | [`Management`](../../doc/models/management.md) | Required | This represent the management container describing the meta information about the event, such as the detection time, the event's location, the source of the event, and the notification distance. | Management getManagement() | setManagement(Management management) |
| `Situation` | [`Situation`](../../doc/models/situation.md) | Optional | This represents the situation container describing the event and the reliability of the detection source. | Situation getSituation() | setSituation(Situation situation) |

## Example

```java
import com.verizon.thingspace.models.ActionId;
import com.verizon.thingspace.models.Altitude;
import com.verizon.thingspace.models.AltitudeConfidenceEnum;
import com.verizon.thingspace.models.AwarenessDistanceEnum;
import com.verizon.thingspace.models.DenmPayload;
import com.verizon.thingspace.models.EventPosition;
import com.verizon.thingspace.models.EventType;
import com.verizon.thingspace.models.Management;
import com.verizon.thingspace.models.PosConfidenceEllipse;
import com.verizon.thingspace.models.Situation;
import com.verizon.thingspace.models.TrafficConditionCauseCode;
import com.verizon.thingspace.models.containers.CauseCodeChoice;

DenmPayload denmPayload = new DenmPayload.Builder(
    new Management.Builder(
        new ActionId.Builder(
            28,
            42
        )
        .build(),
        123456789L,
        123456789L,
        new EventPosition.Builder(
            198,
            234,
            new PosConfidenceEllipse.Builder(
                16,
                114,
                100
            )
            .build(),
            new Altitude.Builder()
                .altitudeValue(236)
                .altitudeConfidence(AltitudeConfidenceEnum.ALT00001)
                .build()
        )
        .build(),
        148
    )
    .awarenessDistance(AwarenessDistanceEnum.LESSTHAN50M)
    .build()
)
.situation(new Situation.Builder(
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
    .build())
.build();
```

