
# Observation Request Attribute

Streaming RF parameter that you want to observe.

## Structure

`ObservationRequestAttribute`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | [`AttributeIdentifierEnum`](../../doc/models/attribute-identifier-enum.md) | Optional | Attribute identifier. | AttributeIdentifierEnum getName() | setName(AttributeIdentifierEnum name) |

## Example

```java
import com.verizon.thingspace.models.AttributeIdentifierEnum;
import com.verizon.thingspace.models.ObservationRequestAttribute;

ObservationRequestAttribute observationRequestAttribute = new ObservationRequestAttribute.Builder()
    .name(AttributeIdentifierEnum.RADIO_SIGNAL_STRENGTH)
    .build();
```

