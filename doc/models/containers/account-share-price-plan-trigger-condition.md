
# Account Share Price Plan Trigger Condition

## Class Name

`AccountSharePricePlanTriggerCondition`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`ConditionTypeEnum`](../../../doc/models/condition-type-enum.md) | AccountSharePricePlanTriggerCondition.fromConditionType(ConditionTypeEnum conditionType) |
| [`ConditionObjectCall`](../../../doc/models/condition-object-call.md) | AccountSharePricePlanTriggerCondition.fromConditionObjectCall(ConditionObjectCall conditionObjectCall) |

## ConditionTypeEnum

### Initialization Code

#### Example

```java
AccountSharePricePlanTriggerCondition.fromConditionType(
        ConditionTypeEnum.AGING
    )
```

## ConditionObjectCall

### Initialization Code

#### Example

```java
AccountSharePricePlanTriggerCondition.fromConditionObjectCall(
        new ConditionObjectCall.Builder()
            .conditionType(ConditionTypeEnum.AGING)
            .comparitor(ComparitorEnum.GT)
            .threshold(100)
            .thresholdUnit(ThresholdUnitEnum.KB)
            .cycleType(RulesCycleTypeEnum.DAILY)
            .build()
    )
```

