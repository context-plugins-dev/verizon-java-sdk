
# Action Id

## Structure

`ActionId`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `OriginatingStationId` | `int` | Required | Unique ID for originating station. | int getOriginatingStationId() | setOriginatingStationId(int originatingStationId) |
| `SequenceNumber` | `int` | Required | Counter used to differenciate multiple DENMs from same station. | int getSequenceNumber() | setSequenceNumber(int sequenceNumber) |

## Example

```java
import com.verizon.thingspace.models.ActionId;

ActionId actionId = new ActionId.Builder(
    28,
    42
)
.build();
```

