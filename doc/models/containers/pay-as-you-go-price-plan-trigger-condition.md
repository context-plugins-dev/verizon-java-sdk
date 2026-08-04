
# Pay as You Go Price Plan Trigger Condition

## Class Name

`PayAsYouGoPricePlanTriggerCondition`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`ConditionTypeEnum`](../../../doc/models/condition-type-enum.md) | PayAsYouGoPricePlanTriggerCondition.fromConditionType(ConditionTypeEnum conditionType) |
| [`ConditionObjectCall`](../../../doc/models/condition-object-call.md) | PayAsYouGoPricePlanTriggerCondition.fromConditionObjectCall(ConditionObjectCall conditionObjectCall) |

## ConditionTypeEnum

### Initialization Code

#### Example

```java
PayAsYouGoPricePlanTriggerCondition.fromConditionType(
        ConditionTypeEnum.AGING
    )
```

## ConditionObjectCall

### Initialization Code

#### Example

```java
PayAsYouGoPricePlanTriggerCondition.fromConditionObjectCall(
        new ConditionObjectCall.Builder()
            .conditionType(ConditionTypeEnum.AGING)
            .comparitor(ComparitorEnum.GT)
            .threshold(100)
            .thresholdUnit(ThresholdUnitEnum.KB)
            .cycleType(RulesCycleTypeEnum.DAILY)
            .build()
    )
```

