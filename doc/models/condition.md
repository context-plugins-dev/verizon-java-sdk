
# Condition

## Structure

`Condition`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Condition` | [`List<Keyschunk2>`](../../doc/models/keyschunk-2.md) | Optional | - | List<Keyschunk2> getCondition() | setCondition(List<Keyschunk2> condition) |

## Example

```java
import com.verizon.thingspace.models.Condition;
import com.verizon.thingspace.models.Keyschunk2;
import java.util.Arrays;

Condition condition = new Condition.Builder()
    .condition(Arrays.asList(
        new Keyschunk2.Builder()
            .dataPercentage50(false)
            .dataPercentage75(false)
            .dataPercentage90(false)
            .dataPercentage100(false)
            .smsPercentage50(false)
            .build()
    ))
    .build();
```

