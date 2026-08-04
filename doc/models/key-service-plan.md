
# Key Service Plan

## Structure

`KeyServicePlan`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Key` | `String` | Optional | - | String getKey() | setKey(String key) |

## Example

```java
import com.verizon.thingspace.models.KeyServicePlan;

KeyServicePlan keyServicePlan = new KeyServicePlan.Builder()
    .key("ServicePlan")
    .build();
```

