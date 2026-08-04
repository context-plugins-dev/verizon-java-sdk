
# Trigger Response

## Structure

`TriggerResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `TriggerId` | `String` | Optional | The system assigned UUID of the trigger | String getTriggerId() | setTriggerId(String triggerId) |

## Example

```java
import com.verizon.thingspace.models.TriggerResponse;

TriggerResponse triggerResponse = new TriggerResponse.Builder()
    .triggerId("be1b5958-ffff-eeee-gggg-b1b7618c0035")
    .build();
```

