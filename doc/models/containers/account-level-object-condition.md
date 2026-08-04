
# Account Level Object Condition

## Class Name

`AccountLevelObjectCondition`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`ConditionTypeEnum`](../../../doc/models/condition-type-enum.md) | AccountLevelObjectCondition.fromConditionType(ConditionTypeEnum conditionType) |
| [`ConditionObjectCall`](../../../doc/models/condition-object-call.md) | AccountLevelObjectCondition.fromConditionObjectCall(ConditionObjectCall conditionObjectCall) |

## ConditionTypeEnum

### Initialization Code

#### Example

```java
AccountLevelObjectCondition.fromConditionType(
        ConditionTypeEnum.AGING
    )
```

## ConditionObjectCall

### Initialization Code

#### Example

```java
AccountLevelObjectCondition.fromConditionObjectCall(
        new ConditionObjectCall.Builder()
            .conditionType(ConditionTypeEnum.AGING)
            .comparitor(ComparitorEnum.GT)
            .threshold(100)
            .thresholdUnit(ThresholdUnitEnum.KB)
            .cycleType(RulesCycleTypeEnum.DAILY)
            .build()
    )
```

