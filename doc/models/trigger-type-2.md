
# Trigger Type 2

Trigger details.

## Structure

`TriggerType2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Anomalyattributes` | [`UsageAnomalyAttributes`](../../doc/models/usage-anomaly-attributes.md) | Optional | The details of the UsageAnomaly trigger. | UsageAnomalyAttributes getAnomalyattributes() | setAnomalyattributes(UsageAnomalyAttributes anomalyattributes) |
| `Notification` | [`TriggerNotification`](../../doc/models/trigger-notification.md) | Optional | The notification details of the trigger. | TriggerNotification getNotification() | setNotification(TriggerNotification notification) |

## Example

```java
import com.verizon.thingspace.models.SMSNumber;
import com.verizon.thingspace.models.TriggerNotification;
import com.verizon.thingspace.models.TriggerType2;
import com.verizon.thingspace.models.UsageAnomalyAttributes;
import java.util.Arrays;

TriggerType2 triggerType2 = new TriggerType2.Builder()
    .anomalyattributes(new UsageAnomalyAttributes.Builder()
        .accountNames("0000123456-00001")
        .deviceGroup("User Group 1")
        .includeAbnormal(true)
        .includeVeryAbnormal(true)
        .includeUnderExpectedUsage(true)
        .includeOverExpectedUsage(true)
        .build())
    .notification(new TriggerNotification.Builder()
        .notificationType("DailySummary")
        .callback(true)
        .emailNotification(true)
        .notificationGroupName("Anomaly Test API")
        .notificationFrequencyFactor(-2147483648)
        .externalEmailRecipients("placeholder@verizon.com")
        .smsNotification(true)
        .smsNumbers(Arrays.asList(
            new SMSNumber.Builder()
                .carrier("US Cellular")
                .number("9299280711")
                .build()
        ))
        .reminder(false)
        .severity("Critical")
        .build())
    .build();
```

