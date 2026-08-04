
# History Attribute Value

Streaming RF parameter for which you want to retrieve history data.

## Structure

`HistoryAttributeValue`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | [`AttributeIdentifierEnum`](../../doc/models/attribute-identifier-enum.md) | Optional | Attribute identifier. | AttributeIdentifierEnum getName() | setName(AttributeIdentifierEnum name) |
| `Value` | `String` | Optional | Attribute value. | String getValue() | setValue(String value) |
| `CreatedOn` | `LocalDateTime` | Optional | Date and time the request was created. | LocalDateTime getCreatedOn() | setCreatedOn(LocalDateTime createdOn) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.AttributeIdentifierEnum;
import com.verizon.thingspace.models.HistoryAttributeValue;

HistoryAttributeValue historyAttributeValue = new HistoryAttributeValue.Builder()
    .name(AttributeIdentifierEnum.LINK_QUALITY)
    .value("47")
    .createdOn(DateTimeHelper.fromRfc8601DateTime("2022-02-10T16:02:21.406Z"))
    .build();
```

