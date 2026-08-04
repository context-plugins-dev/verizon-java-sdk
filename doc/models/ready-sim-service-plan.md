
# Ready Sim Service Plan

## Structure

`ReadySimServicePlan`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ServicePlan` | `String` | Optional | - | String getServicePlan() | setServicePlan(String servicePlan) |

## Example

```java
import com.verizon.thingspace.models.ReadySimServicePlan;

ReadySimServicePlan readySimServicePlan = new ReadySimServicePlan.Builder()
    .servicePlan("123456")
    .build();
```

