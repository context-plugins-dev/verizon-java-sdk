
# Account Level Object

## Structure

`AccountLevelObject`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `FilterCriteria` | [`AccountLevelFilter`](../../doc/models/account-level-filter.md) | Optional | - | AccountLevelFilter getFilterCriteria() | setFilterCriteria(AccountLevelFilter filterCriteria) |
| `Condition` | [`AccountLevelObjectCondition`](../../doc/models/containers/account-level-object-condition.md) | Optional | This is a container for any-of cases. | AccountLevelObjectCondition getCondition() | setCondition(AccountLevelObjectCondition condition) |
| `Action` | [`AccountLevelActionEnum`](../../doc/models/account-level-action-enum.md) | Optional | The action taken when trigger conditions are met | AccountLevelActionEnum getAction() | setAction(AccountLevelActionEnum action) |

## Example

```java
import com.verizon.thingspace.models.AccountLevelActionEnum;
import com.verizon.thingspace.models.AccountLevelFilter;
import com.verizon.thingspace.models.AccountLevelObject;
import com.verizon.thingspace.models.Accountnames;
import com.verizon.thingspace.models.ConditionTypeEnum;
import com.verizon.thingspace.models.containers.AccountLevelObjectCondition;
import java.util.Arrays;

AccountLevelObject accountLevelObject = new AccountLevelObject.Builder()
    .filterCriteria(new AccountLevelFilter.Builder()
        .separateOrCombined("separateOrCombined4")
        .accountNames(new Accountnames.Builder()
            .accountNameList(Arrays.asList(
                "accountNameList7",
                "accountNameList8",
                "accountNameList9"
            ))
            .build())
        .build())
    .condition(AccountLevelObjectCondition.fromConditionType(
        ConditionTypeEnum.USAGEALLOWANCE
    ))
    .action(AccountLevelActionEnum.NOTIFY)
    .build();
```

