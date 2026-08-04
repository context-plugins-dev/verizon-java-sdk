
# Anomaly Trigger Result

A result containing a list of anomaly triggers.

## Structure

`AnomalyTriggerResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Triggers` | [`List<TriggersListOptions2>`](../../doc/models/containers/triggers-list-options-2.md) | Optional | Trigger value chunk details. | List<TriggersListOptions2> getTriggers() | setTriggers(List<TriggersListOptions2> triggers) |

## Example

```java
import com.verizon.thingspace.models.AnomalyTriggerResult;
import com.verizon.thingspace.models.AnomalyTriggerValue;
import com.verizon.thingspace.models.NotificationGroupNameTriggerAttribute;
import com.verizon.thingspace.models.containers.TriggerAttributesOptions2;
import com.verizon.thingspace.models.containers.TriggersListOptions2;
import java.util.Arrays;

AnomalyTriggerResult anomalyTriggerResult = new AnomalyTriggerResult.Builder()
    .triggers(Arrays.asList(
        TriggersListOptions2.fromAnomalyTriggerValue(
            new AnomalyTriggerValue.Builder()
                .triggerId("BE1B5958-3E11-41DB-9ABD-B1B7618C0035")
                .triggerName("Anomaly Daily Usage REST Test-1")
                .organizationName("AnamolyDetectionRTRTest")
                .triggerCategory("UsageAnomaly")
                .triggerAttributes(Arrays.asList(
                    TriggerAttributesOptions2.fromNotificationGroupNameTriggerAttribute(
                        new NotificationGroupNameTriggerAttribute.Builder()
                            .key("DataPercentage50")
                            .build()
                    )
                ))
                .createdAt("2021-10-21T23:57:03.397.0000Z")
                .modifiedAt("2021-10-21T23:57:03.397.0000Z")
                .build()
        )
    ))
    .build();
```

