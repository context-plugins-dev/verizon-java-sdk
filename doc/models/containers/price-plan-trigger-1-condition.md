
# Price Plan Trigger 1 Condition

## Class Name

`PricePlanTrigger1Condition`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`ConditionTypeEnum`](../../../doc/models/condition-type-enum.md) | PricePlanTrigger1Condition.fromConditionType(ConditionTypeEnum conditionType) |
| [`ConditionObjectCall`](../../../doc/models/condition-object-call.md) | PricePlanTrigger1Condition.fromConditionObjectCall(ConditionObjectCall conditionObjectCall) |

## ConditionTypeEnum

### Initialization Code

#### Example

```java
PricePlanTrigger1Condition.fromConditionType(
        ConditionTypeEnum.AGING
    )
```

## ConditionObjectCall

### Initialization Code

#### Example

```java
PricePlanTrigger1Condition.fromConditionObjectCall(
        new ConditionObjectCall.Builder()
            .conditionType(ConditionTypeEnum.AGING)
            .comparitor(ComparitorEnum.GT)
            .threshold(100)
            .thresholdUnit(ThresholdUnitEnum.KB)
            .cycleType(RulesCycleTypeEnum.DAILY)
            .build()
    )
```

