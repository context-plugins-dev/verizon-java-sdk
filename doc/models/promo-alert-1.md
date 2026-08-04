
# Promo Alert 1

## Structure

`PromoAlert1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `FilterCriteria` | `List<Object>` | Optional | - | List<Object> getFilterCriteria() | setFilterCriteria(List<Object> filterCriteria) |
| `Condition` | [`List<Keyschunk2>`](../../doc/models/keyschunk-2.md) | Optional | - | List<Keyschunk2> getCondition() | setCondition(List<Keyschunk2> condition) |
| `EnablePromoExp` | `Boolean` | Optional | - | Boolean getEnablePromoExp() | setEnablePromoExp(Boolean enablePromoExp) |

## Example

```java
import com.verizon.thingspace.ApiHelper;
import com.verizon.thingspace.models.Keyschunk2;
import com.verizon.thingspace.models.PromoAlert1;
import java.io.IOException;
import java.util.Arrays;

PromoAlert1 promoAlert1 = new PromoAlert1.Builder()
    .filterCriteria(Arrays.asList(
        ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}")
    ))
    .condition(Arrays.asList(
        new Keyschunk2.Builder()
            .dataPercentage50(false)
            .dataPercentage75(false)
            .dataPercentage90(false)
            .dataPercentage100(false)
            .smsPercentage50(false)
            .build(),
        new Keyschunk2.Builder()
            .dataPercentage50(false)
            .dataPercentage75(false)
            .dataPercentage90(false)
            .dataPercentage100(false)
            .smsPercentage50(false)
            .build()
    ))
    .enablePromoExp(true)
    .build();
```

