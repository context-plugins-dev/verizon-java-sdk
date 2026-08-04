
# Sae Alert Message

Road Side Alert (RSA) message and its mandatory fields. This message is used to send alerts for nearby hazards to travelers. This message is defined in the SAE J2735 Standard. The system supports all mandatory fields, but only a subset of the optional fields.

## Structure

`SaeAlertMessage`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SaeAlert` | [`SaeAlertPayload`](../../doc/models/sae-alert-payload.md) | Required | Road Side Alert (RSA) message payload as defined in SAE J2735. | SaeAlertPayload getSaeAlert() | setSaeAlert(SaeAlertPayload saeAlert) |

## Example

```java
import com.verizon.thingspace.models.SaeAlertMessage;
import com.verizon.thingspace.models.SaeAlertPayload;
import java.util.Arrays;

SaeAlertMessage saeAlertMessage = new SaeAlertMessage.Builder(
    new SaeAlertPayload.Builder(
        160
    )
    .msgCnt(0)
    .description(Arrays.asList(
            15,
            16
        ))
    .build()
)
.build();
```

