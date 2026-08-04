
# Update Trigger Rules Body

## Class Name

`UpdateTriggerRulesBody`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`AccountLevelUpdateTriggerRequest`](../../../doc/models/account-level-update-trigger-request.md) | UpdateTriggerRulesBody.fromAccountLevelUpdateTriggerRequest(AccountLevelUpdateTriggerRequest accountLevelUpdateTriggerRequest) |
| [`DeviceLevelUpdateTriggerRequest`](../../../doc/models/device-level-update-trigger-request.md) | UpdateTriggerRulesBody.fromDeviceLevelUpdateTriggerRequest(DeviceLevelUpdateTriggerRequest deviceLevelUpdateTriggerRequest) |
| [`AccountGroupShareUpdateTriggerRequest`](../../../doc/models/account-group-share-update-trigger-request.md) | UpdateTriggerRulesBody.fromAccountGroupShareUpdateTriggerRequest(AccountGroupShareUpdateTriggerRequest accountGroupShareUpdateTriggerRequest) |
| [`AccountShareUpdateTriggerRequest`](../../../doc/models/account-share-update-trigger-request.md) | UpdateTriggerRulesBody.fromAccountShareUpdateTriggerRequest(AccountShareUpdateTriggerRequest accountShareUpdateTriggerRequest) |
| [`PayAsYouGoUpdateTriggerRequest`](../../../doc/models/pay-as-you-go-update-trigger-request.md) | UpdateTriggerRulesBody.fromPayAsYouGoUpdateTriggerRequest(PayAsYouGoUpdateTriggerRequest payAsYouGoUpdateTriggerRequest) |
| [`Updatetriggerchunk`](../../../doc/models/updatetriggerchunk.md) | UpdateTriggerRulesBody.fromUpdatetriggerchunk(Updatetriggerchunk updatetriggerchunk) |

## AccountLevelUpdateTriggerRequest

### Initialization Code

#### Example

```java
UpdateTriggerRulesBody.fromAccountLevelUpdateTriggerRequest(
        new AccountLevelUpdateTriggerRequest.Builder()
            .triggerId("be1b5958-ffff-eeee-gggg-b1b7618c0035")
            .triggerName("name of the trigger")
            .ecpdId("Verizon profile ID")
            .notificationType("PerEvent")
            .callback(true)
            .emailNotification(false)
            .notificationGroupName("Notification Group Name (User defined)")
            .notificationFrequencyFactor(3)
            .notificationFrequencyInterval("Daily")
            .externalEmailRecipients("Email addresses")
            .smsNotification(true)
            .reminder(true)
            .severity("Notify")
            .active(ActiveEnum.ENUM_TRUE)
            .build()
    )
```

## DeviceLevelUpdateTriggerRequest

### Initialization Code

#### Example

```java
UpdateTriggerRulesBody.fromDeviceLevelUpdateTriggerRequest(
        new DeviceLevelUpdateTriggerRequest.Builder()
            .triggerId("be1b5958-ffff-eeee-gggg-b1b7618c0035")
            .triggerName("name of the trigger")
            .ecpdId("Verizon profile ID")
            .active(ActiveEnum.ENUM_TRUE)
            .build()
    )
```

## AccountGroupShareUpdateTriggerRequest

### Initialization Code

#### Example

```java
UpdateTriggerRulesBody.fromAccountGroupShareUpdateTriggerRequest(
        new AccountGroupShareUpdateTriggerRequest.Builder()
            .triggerId("be1b5958-ffff-eeee-gggg-b1b7618c0035")
            .triggerName("name of the trigger")
            .accountName("0000123456-00001")
            .active(ActiveEnum.ENUM_TRUE)
            .build()
    )
```

## AccountShareUpdateTriggerRequest

### Initialization Code

#### Example

```java
UpdateTriggerRulesBody.fromAccountShareUpdateTriggerRequest(
        new AccountShareUpdateTriggerRequest.Builder()
            .triggerId("be1b5958-ffff-eeee-gggg-b1b7618c0035")
            .triggerName("name of the trigger")
            .ecpdId("Verizon profile ID")
            .active(ActiveEnum.ENUM_TRUE)
            .build()
    )
```

## PayAsYouGoUpdateTriggerRequest

### Initialization Code

#### Example

```java
UpdateTriggerRulesBody.fromPayAsYouGoUpdateTriggerRequest(
        new PayAsYouGoUpdateTriggerRequest.Builder()
            .triggerId("be1b5958-ffff-eeee-gggg-b1b7618c0035")
            .triggerName("name of the trigger")
            .ecpdId("Verizon profile ID")
            .active(ActiveEnum.ENUM_TRUE)
            .build()
    )
```

## Updatetriggerchunk

### Initialization Code

#### Example

```java
UpdateTriggerRulesBody.fromUpdatetriggerchunk(
        new Updatetriggerchunk.Builder()
            .triggerId("be1b5958-ffff-eeee-gggg-b1b7618c0035")
            .triggerName("name of the trigger")
            .ecpdId("Verizon profile ID")
            .active(ActiveEnum.ENUM_TRUE)
            .build()
    )
```

