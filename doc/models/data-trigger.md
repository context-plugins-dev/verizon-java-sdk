
# Data Trigger

## Structure

`DataTrigger`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountLevel` | [`AccountLevelObject`](../../doc/models/account-level-object.md) | Optional | - | AccountLevelObject getAccountLevel() | setAccountLevel(AccountLevelObject accountLevel) |

## Example

```java
import com.verizon.thingspace.models.AccountLevelActionEnum;
import com.verizon.thingspace.models.AccountLevelFilter;
import com.verizon.thingspace.models.AccountLevelObject;
import com.verizon.thingspace.models.Accountnames;
import com.verizon.thingspace.models.ConditionTypeEnum;
import com.verizon.thingspace.models.DataTrigger;
import com.verizon.thingspace.models.containers.AccountLevelObjectCondition;
import java.util.Arrays;

DataTrigger dataTrigger = new DataTrigger.Builder()
    .accountLevel(new AccountLevelObject.Builder()
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
            ConditionTypeEnum.INDIVIDUAL
        ))
        .action(AccountLevelActionEnum.SUSPEND)
        .build())
    .build();
```

