
# Active Trigger Indicator

Whether the trigger is active or not.

## Structure

`ActiveTriggerIndicator`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Active` | `Boolean` | Optional | Indicates if the trigger is active<br />True - trigger is active<br />False - trigger is not active. | Boolean getActive() | setActive(Boolean active) |

## Example

```java
import com.verizon.thingspace.models.ActiveTriggerIndicator;

ActiveTriggerIndicator activeTriggerIndicator = new ActiveTriggerIndicator.Builder()
    .active(true)
    .build();
```

