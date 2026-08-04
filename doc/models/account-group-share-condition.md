
# Account Group Share Condition

## Structure

`AccountGroupShareCondition`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Action` | [`ConditionActionEnum`](../../doc/models/condition-action-enum.md) | Optional | The action taken when trigger conditions are met | ConditionActionEnum getAction() | setAction(ConditionActionEnum action) |

## Example

```java
import com.verizon.thingspace.models.AccountGroupShareCondition;
import com.verizon.thingspace.models.ConditionActionEnum;

AccountGroupShareCondition accountGroupShareCondition = new AccountGroupShareCondition.Builder()
    .action(ConditionActionEnum.NOTIFY)
    .build();
```

