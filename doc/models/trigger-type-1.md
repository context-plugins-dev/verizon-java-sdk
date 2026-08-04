
# Trigger Type 1

Trigger details.

## Structure

`TriggerType1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Optional | Trigger name. | String getName() | setName(String name) |
| `TriggerCategory` | `String` | Optional | This is the value to use in the request body to detect anomalous behaivior. The values in this table will only be relevant when this parameter is set to this value. | String getTriggerCategory() | setTriggerCategory(String triggerCategory) |
| `AccountName` | `String` | Optional | Account name.<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `32` | String getAccountName() | setAccountName(String accountName) |
| `AnomalyTriggerRequest` | [`AnomalyTriggerRequest`](../../doc/models/anomaly-trigger-request.md) | Optional | The details of the UsageAnomaly trigger. | AnomalyTriggerRequest getAnomalyTriggerRequest() | setAnomalyTriggerRequest(AnomalyTriggerRequest anomalyTriggerRequest) |
| `Notification` | [`TriggerNotification`](../../doc/models/trigger-notification.md) | Optional | The notification details of the trigger. | TriggerNotification getNotification() | setNotification(TriggerNotification notification) |

## Example

```java
import com.verizon.thingspace.models.AnomalyTriggerRequest;
import com.verizon.thingspace.models.SMSNumber;
import com.verizon.thingspace.models.TriggerNotification;
import com.verizon.thingspace.models.TriggerType1;
import java.util.Arrays;

TriggerType1 triggerType1 = new TriggerType1.Builder()
    .name("Anomaly Daily Usage REST Test-Patch 1")
    .triggerCategory("UsageAnomaly")
    .accountName("0000123456-00001")
    .anomalyTriggerRequest(new AnomalyTriggerRequest.Builder()
        .accountNames("0000123456-00001")
        .includeAbnormal(true)
        .includeVeryAbnormal(true)
        .includeUnderExpectedUsage(true)
        .includeOverExpectedUsage(true)
        .build())
    .notification(new TriggerNotification.Builder()
        .notificationType("DailySummary")
        .callback(true)
        .emailNotification(false)
        .notificationGroupName("Anomaly Test API")
        .notificationFrequencyFactor(3)
        .notificationFrequencyInterval("Hourly")
        .externalEmailRecipients("placeholder@verizon.com")
        .smsNotification(true)
        .smsNumbers(Arrays.asList(
            new SMSNumber.Builder()
                .carrier("US Cellular")
                .number("9299280711")
                .build()
        ))
        .reminder(true)
        .severity("Critical")
        .build())
    .build();
```

