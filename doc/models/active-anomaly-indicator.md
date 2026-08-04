
# Active Anomaly Indicator

Whether the anomaly detection is active or not.

## Structure

`ActiveAnomalyIndicator`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Active` | `Boolean` | Optional | Indicates anomaly detection is active<br />True - Anomaly detection is active.<br />False - Anomaly detection is not active. | Boolean getActive() | setActive(Boolean active) |

## Example

```java
import com.verizon.thingspace.models.ActiveAnomalyIndicator;

ActiveAnomalyIndicator activeAnomalyIndicator = new ActiveAnomalyIndicator.Builder()
    .active(true)
    .build();
```

