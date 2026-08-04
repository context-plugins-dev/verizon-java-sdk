
# Generic Message

A message carrying a generic (custom) V2X payload.

## Structure

`GenericMessage`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Generic` | [`GenericPayload`](../../doc/models/generic-payload.md) | Required | Custom message which is defined by the user and can support "any" message type or format.<br><br>**Note:** ETX prefers the j2735 or the j2735_gr encoding and only vendor specific message types are allowed to be published in different message formats. | GenericPayload getGeneric() | setGeneric(GenericPayload generic) |

## Example

```java
import com.verizon.thingspace.models.GenericMessage;
import com.verizon.thingspace.models.GenericPayload;

GenericMessage genericMessage = new GenericMessage.Builder(
    new GenericPayload.Builder(
        "messageType4",
        "messageFormat6",
        "payload0"
    )
    .build()
)
.build();
```

