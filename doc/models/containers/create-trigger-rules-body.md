
# Create Trigger Rules Body

## Class Name

`CreateTriggerRulesBody`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`AccountLevelCreateTriggerRequest`](../../../doc/models/account-level-create-trigger-request.md) | CreateTriggerRulesBody.fromAccountLevelCreateTriggerRequest(AccountLevelCreateTriggerRequest accountLevelCreateTriggerRequest) |
| [`AccountLevelObject`](../../../doc/models/account-level-object.md) | CreateTriggerRulesBody.fromAccountLevelObject(AccountLevelObject accountLevelObject) |
| [`DeviceLevelCreateTriggerRequest`](../../../doc/models/device-level-create-trigger-request.md) | CreateTriggerRulesBody.fromDeviceLevelCreateTriggerRequest(DeviceLevelCreateTriggerRequest deviceLevelCreateTriggerRequest) |
| [`AccountGroupShareCreateTriggerRequest`](../../../doc/models/account-group-share-create-trigger-request.md) | CreateTriggerRulesBody.fromAccountGroupShareCreateTriggerRequest(AccountGroupShareCreateTriggerRequest accountGroupShareCreateTriggerRequest) |
| [`AccountShareCreateTriggerRequest`](../../../doc/models/account-share-create-trigger-request.md) | CreateTriggerRulesBody.fromAccountShareCreateTriggerRequest(AccountShareCreateTriggerRequest accountShareCreateTriggerRequest) |
| [`PayAsYouGoCreateTriggerRequest`](../../../doc/models/pay-as-you-go-create-trigger-request.md) | CreateTriggerRulesBody.fromPayAsYouGoCreateTriggerRequest(PayAsYouGoCreateTriggerRequest payAsYouGoCreateTriggerRequest) |
| [`Createtriggerchunk`](../../../doc/models/createtriggerchunk.md) | CreateTriggerRulesBody.fromCreatetriggerchunk(Createtriggerchunk createtriggerchunk) |

## AccountLevelCreateTriggerRequest

### Initialization Code

#### Example

```java
CreateTriggerRulesBody.fromAccountLevelCreateTriggerRequest(
        new AccountLevelCreateTriggerRequest.Builder()
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

## AccountLevelObject

### Initialization Code

#### Example

```java
CreateTriggerRulesBody.fromAccountLevelObject(
        new AccountLevelObject.Builder()
            .action(AccountLevelActionEnum.NOTIFY)
            .build()
    )
```

## DeviceLevelCreateTriggerRequest

### Initialization Code

#### Example

```java
CreateTriggerRulesBody.fromDeviceLevelCreateTriggerRequest(
        new DeviceLevelCreateTriggerRequest.Builder()
            .triggerName("name of the trigger")
            .ecpdId("Verizon profile ID")
            .active(ActiveEnum.ENUM_TRUE)
            .build()
    )
```

## AccountGroupShareCreateTriggerRequest

### Initialization Code

#### Example

```java
CreateTriggerRulesBody.fromAccountGroupShareCreateTriggerRequest(
        new AccountGroupShareCreateTriggerRequest.Builder()
            .triggerName("name of the trigger")
            .accountName("0000123456-00001")
            .active(ActiveEnum.ENUM_TRUE)
            .build()
    )
```

## AccountShareCreateTriggerRequest

### Initialization Code

#### Example

```java
CreateTriggerRulesBody.fromAccountShareCreateTriggerRequest(
        new AccountShareCreateTriggerRequest.Builder()
            .triggerName("name of the trigger")
            .ecpdId("Verizon profile ID")
            .active(ActiveEnum.ENUM_TRUE)
            .build()
    )
```

## PayAsYouGoCreateTriggerRequest

### Initialization Code

#### Example

```java
CreateTriggerRulesBody.fromPayAsYouGoCreateTriggerRequest(
        new PayAsYouGoCreateTriggerRequest.Builder()
            .triggerName("name of the trigger")
            .ecpdId("Verizon profile ID")
            .active(ActiveEnum.ENUM_TRUE)
            .build()
    )
```

## Createtriggerchunk

### Initialization Code

#### Example

```java
CreateTriggerRulesBody.fromCreatetriggerchunk(
        new Createtriggerchunk.Builder()
            .triggerName("name of the trigger")
            .ecpdId("Verizon profile ID")
            .active(ActiveEnum.ENUM_TRUE)
            .build()
    )
```

