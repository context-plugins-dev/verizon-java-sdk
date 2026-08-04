
# Create Trigger Request Options 2

## Class Name

`CreateTriggerRequestOptions2`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`TriggerType1`](../../../doc/models/trigger-type-1.md) | CreateTriggerRequestOptions2.fromTriggerType1(TriggerType1 triggerType1) |
| [`ActiveAnomalyIndicator`](../../../doc/models/active-anomaly-indicator.md) | CreateTriggerRequestOptions2.fromActiveAnomalyIndicator(ActiveAnomalyIndicator activeAnomalyIndicator) |
| [`ActiveTriggerIndicator`](../../../doc/models/active-trigger-indicator.md) | CreateTriggerRequestOptions2.fromActiveTriggerIndicator(ActiveTriggerIndicator activeTriggerIndicator) |

## TriggerType1

### Initialization Code

#### Example

```java
CreateTriggerRequestOptions2.fromTriggerType1(
        new TriggerType1.Builder()
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
            .build()
    )
```

## ActiveAnomalyIndicator

### Initialization Code

#### Example

```java
CreateTriggerRequestOptions2.fromActiveAnomalyIndicator(
        new ActiveAnomalyIndicator.Builder()
            .active(true)
            .build()
    )
```

## ActiveTriggerIndicator

### Initialization Code

#### Example

```java
CreateTriggerRequestOptions2.fromActiveTriggerIndicator(
        new ActiveTriggerIndicator.Builder()
            .active(true)
            .build()
    )
```

