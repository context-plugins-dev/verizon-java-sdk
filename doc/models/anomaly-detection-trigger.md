
# Anomaly Detection Trigger

Trigger for anomaly detection.

## Structure

`AnomalyDetectionTrigger`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `TriggerId` | `String` | Optional | Trigger ID to identify the request in a callback. | String getTriggerId() | setTriggerId(String triggerId) |

## Example

```java
import com.verizon.thingspace.models.AnomalyDetectionTrigger;

AnomalyDetectionTrigger anomalyDetectionTrigger = new AnomalyDetectionTrigger.Builder()
    .triggerId("595f5c44-c31c-4552-8670-020a1545a84d")
    .build();
```

