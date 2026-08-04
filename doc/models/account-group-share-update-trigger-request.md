
# Account Group Share Update Trigger Request

## Structure

`AccountGroupShareUpdateTriggerRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `TriggerId` | `String` | Optional | The system assigned UUID of the trigger | String getTriggerId() | setTriggerId(String triggerId) |
| `TriggerName` | `String` | Optional | The user defined name of the trigger | String getTriggerName() | setTriggerName(String triggerName) |
| `AccountName` | `String` | Optional | The numeric name of the account and must include leading zeroes | String getAccountName() | setAccountName(String accountName) |
| `TriggerCategory` | [`TriggerCategoryEnum`](../../doc/models/trigger-category-enum.md) | Optional | The type of trigger being created or modified | TriggerCategoryEnum getTriggerCategory() | setTriggerCategory(TriggerCategoryEnum triggerCategory) |
| `DataTrigger` | [`AccountGroupShareObject`](../../doc/models/account-group-share-object.md) | Optional | - | AccountGroupShareObject getDataTrigger() | setDataTrigger(AccountGroupShareObject dataTrigger) |
| `Notification` | [`Notificationarray`](../../doc/models/notificationarray.md) | Optional | - | Notificationarray getNotification() | setNotification(Notificationarray notification) |
| `Active` | [`ActiveEnum`](../../doc/models/active-enum.md) | Optional | A flag to indicate of the trigger is active, true, or not, false | ActiveEnum getActive() | setActive(ActiveEnum active) |

## Example

```java
import com.verizon.thingspace.models.AccountGroupShareAction;
import com.verizon.thingspace.models.AccountGroupShareCondition;
import com.verizon.thingspace.models.AccountGroupShareFilter;
import com.verizon.thingspace.models.AccountGroupShareFilterCriteria;
import com.verizon.thingspace.models.AccountGroupShareIndividual1;
import com.verizon.thingspace.models.AccountGroupShareObject;
import com.verizon.thingspace.models.AccountGroupShareUpdateTriggerRequest;
import com.verizon.thingspace.models.ActiveEnum;
import com.verizon.thingspace.models.AllowanceThreshold;
import com.verizon.thingspace.models.Carriercode1;
import com.verizon.thingspace.models.ConditionActionEnum;
import com.verizon.thingspace.models.Notify;
import com.verizon.thingspace.models.TriggerCategoryEnum;
import com.verizon.thingspace.models.containers.NotifyThreshold;
import java.util.Arrays;

AccountGroupShareUpdateTriggerRequest accountGroupShareUpdateTriggerRequest = new AccountGroupShareUpdateTriggerRequest.Builder()
    .triggerId("be1b5958-ffff-eeee-gggg-b1b7618c0035")
    .triggerName("name of the trigger")
    .accountName("0000123456-00001")
    .triggerCategory(TriggerCategoryEnum.ACCOUNTUSAGE)
    .dataTrigger(new AccountGroupShareObject.Builder()
        .accountGroupShare(new AccountGroupShareIndividual1.Builder()
            .accountGroupShareIndividual(new AccountGroupShareFilterCriteria.Builder()
                .filterCriteria(new AccountGroupShareFilter.Builder()
                    .ratePlanGroupId(202)
                    .build())
                .condition(new AccountGroupShareCondition.Builder()
                    .action(ConditionActionEnum.NOTIFY)
                    .build())
                .action(new AccountGroupShareAction.Builder()
                    .notify(new Notify.Builder()
                        .alertType("alertType8")
                        .threshold(Arrays.asList(
                            NotifyThreshold.fromCarriercode1(
                                new Carriercode1.Builder()
                                    .carrierCode("carrierCode4")
                                    .percentage(new AllowanceThreshold.Builder()
                                        .percentage50(false)
                                        .percentage75(false)
                                        .percentage90(false)
                                        .percentage100(false)
                                        .build())
                                    .build()
                            ),
                            NotifyThreshold.fromCarriercode1(
                                new Carriercode1.Builder()
                                    .carrierCode("carrierCode4")
                                    .percentage(new AllowanceThreshold.Builder()
                                        .percentage50(false)
                                        .percentage75(false)
                                        .percentage90(false)
                                        .percentage100(false)
                                        .build())
                                    .build()
                            ),
                            NotifyThreshold.fromCarriercode1(
                                new Carriercode1.Builder()
                                    .carrierCode("carrierCode4")
                                    .percentage(new AllowanceThreshold.Builder()
                                        .percentage50(false)
                                        .percentage75(false)
                                        .percentage90(false)
                                        .percentage100(false)
                                        .build())
                                    .build()
                            )
                        ))
                        .build())
                    .build())
                .build())
            .build())
        .build())
    .active(ActiveEnum.ENUM_TRUE)
    .build();
```

