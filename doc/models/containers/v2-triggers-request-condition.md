
# V2 Triggers Request Condition

## Class Name

`V2TriggersRequestCondition`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`ConditionTypeEnum`](../../../doc/models/condition-type-enum.md) | V2TriggersRequestCondition.fromConditionType(ConditionTypeEnum conditionType) |
| [`ConditionObjectCall`](../../../doc/models/condition-object-call.md) | V2TriggersRequestCondition.fromConditionObjectCall(ConditionObjectCall conditionObjectCall) |

## ConditionTypeEnum

### Initialization Code

#### Example

```java
V2TriggersRequestCondition.fromConditionType(
        ConditionTypeEnum.AGING
    )
```

## ConditionObjectCall

### Initialization Code

#### Example

```java
V2TriggersRequestCondition.fromConditionObjectCall(
        new ConditionObjectCall.Builder()
            .conditionType(ConditionTypeEnum.AGING)
            .comparitor(ComparitorEnum.GT)
            .threshold(100)
            .thresholdUnit(ThresholdUnitEnum.KB)
            .cycleType(RulesCycleTypeEnum.DAILY)
            .build()
    )
```

