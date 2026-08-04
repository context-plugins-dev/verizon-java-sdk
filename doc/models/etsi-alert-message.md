
# Etsi Alert Message

Decentralized Environmental Notification Message (DENM) message and its mandatory fields. It is used in order to alert road users of a detected event using ITS communication technologies.

## Structure

`EtsiAlertMessage`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `EtsiAlert` | [`EtsiAlertPayload`](../../doc/models/etsi-alert-payload.md) | Required | DENM (Decentralized Environmental Notification Message) payload as defined in ETSI. | EtsiAlertPayload getEtsiAlert() | setEtsiAlert(EtsiAlertPayload etsiAlert) |

## Example

```java
import com.verizon.thingspace.models.ActionId;
import com.verizon.thingspace.models.Altitude;
import com.verizon.thingspace.models.AltitudeConfidenceEnum;
import com.verizon.thingspace.models.AwarenessDistanceEnum;
import com.verizon.thingspace.models.DenmPayload;
import com.verizon.thingspace.models.EtsiAlertMessage;
import com.verizon.thingspace.models.EtsiAlertPayload;
import com.verizon.thingspace.models.EventPosition;
import com.verizon.thingspace.models.EventType;
import com.verizon.thingspace.models.Header;
import com.verizon.thingspace.models.Management;
import com.verizon.thingspace.models.MessageIdEnum;
import com.verizon.thingspace.models.PosConfidenceEllipse;
import com.verizon.thingspace.models.ProtocolVersionEnum;
import com.verizon.thingspace.models.Situation;
import com.verizon.thingspace.models.TrafficConditionCauseCode;
import com.verizon.thingspace.models.containers.CauseCodeChoice;

EtsiAlertMessage etsiAlertMessage = new EtsiAlertMessage.Builder(
    new EtsiAlertPayload.Builder(
        new Header.Builder(
            ProtocolVersionEnum.ENUM_2,
            MessageIdEnum.ENUM_1,
            12345
        )
        .build(),
        new DenmPayload.Builder(
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
        .build()
    )
    .build()
)
.build();
```

