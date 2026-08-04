
# Triggers List Options 2

## Class Name

`TriggersListOptions2`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`AnomalyTriggerValue`](../../../doc/models/anomaly-trigger-value.md) | TriggersListOptions2.fromAnomalyTriggerValue(AnomalyTriggerValue anomalyTriggerValue) |
| [`TriggerType2`](../../../doc/models/trigger-type-2.md) | TriggersListOptions2.fromTriggerType2(TriggerType2 triggerType2) |

## AnomalyTriggerValue

### Initialization Code

#### Example

```java
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
```

## TriggerType2

### Initialization Code

#### Example

```java
TriggersListOptions2.fromTriggerType2(
        new TriggerType2.Builder()
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
            .build()
    )
```

