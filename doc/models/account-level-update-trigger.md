
# Account Level Update Trigger

## Structure

`AccountLevelUpdateTrigger`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `TriggerId` | `String` | Optional | The system assigned UUID of the trigger | String getTriggerId() | setTriggerId(String triggerId) |
| `TriggerName` | `String` | Optional | The user defined name of the trigger | String getTriggerName() | setTriggerName(String triggerName) |
| `EcpdId` | `String` | Optional | The Enterprise Customer Profile Database ID | String getEcpdId() | setEcpdId(String ecpdId) |
| `TriggerCategory` | [`TriggerCategoryEnum`](../../doc/models/trigger-category-enum.md) | Optional | The type of trigger being created or modified | TriggerCategoryEnum getTriggerCategory() | setTriggerCategory(TriggerCategoryEnum triggerCategory) |
| `DataTrigger` | [`DataTrigger1`](../../doc/models/data-trigger-1.md) | Optional | - | DataTrigger1 getDataTrigger() | setDataTrigger(DataTrigger1 dataTrigger) |
| `Notification` | [`Notificationarray`](../../doc/models/notificationarray.md) | Optional | - | Notificationarray getNotification() | setNotification(Notificationarray notification) |

## Example

```java
import com.verizon.thingspace.models.AccountLevelActionEnum;
import com.verizon.thingspace.models.AccountLevelFilter;
import com.verizon.thingspace.models.AccountLevelUpdateTrigger;
import com.verizon.thingspace.models.Accountnames;
import com.verizon.thingspace.models.ComparitorEnum;
import com.verizon.thingspace.models.ConditionTypeEnum;
import com.verizon.thingspace.models.DataTrigger1;
import com.verizon.thingspace.models.TriggerCategoryEnum;
import com.verizon.thingspace.models.containers.DataTrigger1Condition;
import java.util.Arrays;

AccountLevelUpdateTrigger accountLevelUpdateTrigger = new AccountLevelUpdateTrigger.Builder()
    .triggerId("be1b5958-ffff-eeee-gggg-b1b7618c0035")
    .triggerName("name of the trigger")
    .ecpdId("Verizon profile ID")
    .triggerCategory(TriggerCategoryEnum.DEVICEGROUPUSAGE)
    .dataTrigger(new DataTrigger1.Builder()
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
        .condition(DataTrigger1Condition.fromConditionType(
            ConditionTypeEnum.USAGEALLOWANCE
        ))
        .action(AccountLevelActionEnum.NOTIFY)
        .conditionType(ConditionTypeEnum.AGING)
        .comparitor(ComparitorEnum.EQ)
        .build())
    .build();
```

