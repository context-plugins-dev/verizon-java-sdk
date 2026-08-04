
# History Search Filter Attributes

Streaming RF parameters for which you want to retrieve history data.

## Structure

`HistorySearchFilterAttributes`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | [`AttributeIdentifierEnum`](../../doc/models/attribute-identifier-enum.md) | Optional | Attribute identifier. | AttributeIdentifierEnum getName() | setName(AttributeIdentifierEnum name) |

## Example

```java
import com.verizon.thingspace.models.AttributeIdentifierEnum;
import com.verizon.thingspace.models.HistorySearchFilterAttributes;

HistorySearchFilterAttributes historySearchFilterAttributes = new HistorySearchFilterAttributes.Builder()
    .name(AttributeIdentifierEnum.LINK_QUALITY)
    .build();
```

