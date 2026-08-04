
# Account Level Create Trigger

## Structure

`AccountLevelCreateTrigger`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `TriggerName` | `String` | Optional | The user defined name of the trigger | String getTriggerName() | setTriggerName(String triggerName) |
| `EcpdId` | `String` | Optional | The Enterprise Customer Profile Database ID | String getEcpdId() | setEcpdId(String ecpdId) |
| `TriggerCategory` | [`TriggerCategoryEnum`](../../doc/models/trigger-category-enum.md) | Optional | The type of trigger being created or modified | TriggerCategoryEnum getTriggerCategory() | setTriggerCategory(TriggerCategoryEnum triggerCategory) |
| `DataTrigger` | [`DataTrigger`](../../doc/models/data-trigger.md) | Optional | - | DataTrigger getDataTrigger() | setDataTrigger(DataTrigger dataTrigger) |
| `Notification` | [`Notificationarray`](../../doc/models/notificationarray.md) | Optional | - | Notificationarray getNotification() | setNotification(Notificationarray notification) |

## Example

```java
import com.verizon.thingspace.models.AccountLevelActionEnum;
import com.verizon.thingspace.models.AccountLevelCreateTrigger;
import com.verizon.thingspace.models.AccountLevelFilter;
import com.verizon.thingspace.models.AccountLevelObject;
import com.verizon.thingspace.models.Accountnames;
import com.verizon.thingspace.models.ConditionTypeEnum;
import com.verizon.thingspace.models.DataTrigger;
import com.verizon.thingspace.models.Notificationarray;
import com.verizon.thingspace.models.TriggerCategoryEnum;
import com.verizon.thingspace.models.containers.AccountLevelObjectCondition;
import java.util.Arrays;

AccountLevelCreateTrigger accountLevelCreateTrigger = new AccountLevelCreateTrigger.Builder()
    .triggerName("name of the trigger")
    .ecpdId("Verizon profile ID")
    .triggerCategory(TriggerCategoryEnum.ACCOUNTUSAGE)
    .dataTrigger(new DataTrigger.Builder()
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
        .build())
    .notification(new Notificationarray.Builder()
        .notificationType("notificationType8")
        .callback(false)
        .emailNotification(false)
        .notificationGroupName("notificationGroupName6")
        .notificationFrequencyFactor(22)
        .build())
    .build();
```

