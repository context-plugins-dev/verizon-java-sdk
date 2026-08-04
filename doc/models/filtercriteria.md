
# Filtercriteria

## Structure

`Filtercriteria`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `FilterCriteria` | [`List<ReadySimServicePlan>`](../../doc/models/ready-sim-service-plan.md) | Optional | - | List<ReadySimServicePlan> getFilterCriteria() | setFilterCriteria(List<ReadySimServicePlan> filterCriteria) |

## Example

```java
import com.verizon.thingspace.models.Filtercriteria;
import com.verizon.thingspace.models.ReadySimServicePlan;
import java.util.Arrays;

Filtercriteria filtercriteria = new Filtercriteria.Builder()
    .filterCriteria(Arrays.asList(
        new ReadySimServicePlan.Builder()
            .servicePlan("servicePlan4")
            .build()
    ))
    .build();
```

