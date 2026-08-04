
# Data Percentage 50 Trigger Attribute

Trigger attribute for when data percentage is over 50% used.

## Structure

`DataPercentage50TriggerAttribute`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Key` | `String` | Optional | Key data percentage 50. | String getKey() | setKey(String key) |
| `Value` | `Boolean` | Optional | DataPercentage50<br />True - Trigger on Data percentage is over 50% used<br />False - Do not trigger when over 50% used. | Boolean getValue() | setValue(Boolean value) |

## Example

```java
import com.verizon.thingspace.models.DataPercentage50TriggerAttribute;

DataPercentage50TriggerAttribute dataPercentage50TriggerAttribute = new DataPercentage50TriggerAttribute.Builder()
    .key("DataPercentage50")
    .value(false)
    .build();
```

