
# Promo Alert

## Structure

`PromoAlert`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `FilterCriteria` | [`List<ReadySimServicePlan>`](../../doc/models/ready-sim-service-plan.md) | Optional | - | List<ReadySimServicePlan> getFilterCriteria() | setFilterCriteria(List<ReadySimServicePlan> filterCriteria) |
| `Condition` | [`List<Keyschunk2>`](../../doc/models/keyschunk-2.md) | Optional | - | List<Keyschunk2> getCondition() | setCondition(List<Keyschunk2> condition) |
| `EnablePromoExp` | `Boolean` | Optional | - | Boolean getEnablePromoExp() | setEnablePromoExp(Boolean enablePromoExp) |

## Example

```java
import com.verizon.thingspace.models.Keyschunk2;
import com.verizon.thingspace.models.PromoAlert;
import com.verizon.thingspace.models.ReadySimServicePlan;
import java.util.Arrays;

PromoAlert promoAlert = new PromoAlert.Builder()
    .filterCriteria(Arrays.asList(
        new ReadySimServicePlan.Builder()
            .servicePlan("servicePlan4")
            .build(),
        new ReadySimServicePlan.Builder()
            .servicePlan("servicePlan4")
            .build()
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

