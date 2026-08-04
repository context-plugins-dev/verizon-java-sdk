
# Service Plan Trigger Attribute

Key service plan trigger attribute.

## Structure

`ServicePlanTriggerAttribute`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Key` | `String` | Optional | The ServicePlan name will be listed here. | String getKey() | setKey(String key) |

## Example

```java
import com.verizon.thingspace.models.ServicePlanTriggerAttribute;

ServicePlanTriggerAttribute servicePlanTriggerAttribute = new ServicePlanTriggerAttribute.Builder()
    .key("ServicePlan")
    .build();
```

