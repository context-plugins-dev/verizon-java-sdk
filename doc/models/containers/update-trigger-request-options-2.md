
# Update Trigger Request Options 2

## Class Name

`UpdateTriggerRequestOptions2`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`TriggerType3`](../../../doc/models/trigger-type-3.md) | UpdateTriggerRequestOptions2.fromTriggerType3(TriggerType3 triggerType3) |
| [`ActiveAnomalyIndicator`](../../../doc/models/active-anomaly-indicator.md) | UpdateTriggerRequestOptions2.fromActiveAnomalyIndicator(ActiveAnomalyIndicator activeAnomalyIndicator) |

## TriggerType3

### Initialization Code

#### Example

```java
UpdateTriggerRequestOptions2.fromTriggerType3(
        new TriggerType3.Builder()
            .triggerId("595f5c44-c31c-4552-8670-020a1545a84d")
            .triggerName("Anomaly Daily Usage REST Test-Patch Update 4")
            .triggerCategory("UsageAnomaly")
            .accountName("0000123456-00001")
            .anomalyTriggerRequest(new AnomalyTriggerRequest.Builder()
                .accountNames("0000123456-00001")
                .includeAbnormal(true)
                .includeVeryAbnormal(true)
                .includeUnderExpectedUsage(false)
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
            .build()
    )
```

## ActiveAnomalyIndicator

### Initialization Code

#### Example

```java
UpdateTriggerRequestOptions2.fromActiveAnomalyIndicator(
        new ActiveAnomalyIndicator.Builder()
            .active(true)
            .build()
    )
```

