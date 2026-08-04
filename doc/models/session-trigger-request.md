
# Session Trigger Request

## Structure

`SessionTriggerRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Comparator` | `String` | Optional | **Constraints**: *Minimum Length*: `3`, *Maximum Length*: `32`, *Pattern*: `^[A-Za-z0-9]{3,32}$` | String getComparator() | setComparator(String comparator) |
| `Threshold` | `Integer` | Optional | **Constraints**: `>= 0`, `<= 100` | Integer getThreshold() | setThreshold(Integer threshold) |

## Example

```java
import com.verizon.thingspace.models.SessionTriggerRequest;

SessionTriggerRequest sessionTriggerRequest = new SessionTriggerRequest.Builder()
    .comparator("comparator6")
    .threshold(100)
    .build();
```

