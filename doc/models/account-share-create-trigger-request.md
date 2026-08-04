
# Account Share Create Trigger Request

## Structure

`AccountShareCreateTriggerRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `TriggerName` | `String` | Optional | The user defined name of the trigger | String getTriggerName() | setTriggerName(String triggerName) |
| `EcpdId` | `String` | Optional | The Enterprise Customer Profile Database ID | String getEcpdId() | setEcpdId(String ecpdId) |
| `TriggerCategory` | [`TriggerCategoryEnum`](../../doc/models/trigger-category-enum.md) | Optional | The type of trigger being created or modified | TriggerCategoryEnum getTriggerCategory() | setTriggerCategory(TriggerCategoryEnum triggerCategory) |
| `PricePlanTrigger` | [`AccountSharePricePlanTrigger`](../../doc/models/account-share-price-plan-trigger.md) | Optional | - | AccountSharePricePlanTrigger getPricePlanTrigger() | setPricePlanTrigger(AccountSharePricePlanTrigger pricePlanTrigger) |
| `Notification` | [`Notificationarray`](../../doc/models/notificationarray.md) | Optional | - | Notificationarray getNotification() | setNotification(Notificationarray notification) |
| `Active` | [`ActiveEnum`](../../doc/models/active-enum.md) | Optional | A flag to indicate of the trigger is active, true, or not, false | ActiveEnum getActive() | setActive(ActiveEnum active) |

## Example

```java
import com.verizon.thingspace.models.AccountShareCreateTriggerRequest;
import com.verizon.thingspace.models.AccountShareFilterCriteria;
import com.verizon.thingspace.models.AccountShareFilterCriteria1;
import com.verizon.thingspace.models.AccountSharePricePlanTrigger;
import com.verizon.thingspace.models.ActiveEnum;
import com.verizon.thingspace.models.ChangePlanDetails;
import com.verizon.thingspace.models.ConditionTypeEnum;
import com.verizon.thingspace.models.Notificationarray;
import com.verizon.thingspace.models.TriggerCategoryEnum;
import com.verizon.thingspace.models.containers.AccountSharePricePlanTriggerCondition;
import java.util.Arrays;

AccountShareCreateTriggerRequest accountShareCreateTriggerRequest = new AccountShareCreateTriggerRequest.Builder()
    .triggerName("name of the trigger")
    .ecpdId("Verizon profile ID")
    .triggerCategory(TriggerCategoryEnum.DEVICEGROUPUSAGE)
    .pricePlanTrigger(new AccountSharePricePlanTrigger.Builder()
        .accountShare(new AccountShareFilterCriteria.Builder()
            .filterCriteria(new AccountShareFilterCriteria1.Builder()
                .carrierServicePlanCode("carrierServicePlanCode4")
                .accountNameList(Arrays.asList(
                    "accountNameList7",
                    "accountNameList8"
                ))
                .build())
            .build())
        .condition(AccountSharePricePlanTriggerCondition.fromConditionType(
            ConditionTypeEnum.AGING
        ))
        .changePlan(false)
        .changePlanDetails(new ChangePlanDetails.Builder()
            .toCarrierServicePlanCode("toCarrierServicePlanCode2")
            .build())
        .build())
    .notification(new Notificationarray.Builder()
        .notificationType("notificationType8")
        .callback(false)
        .emailNotification(false)
        .notificationGroupName("notificationGroupName6")
        .notificationFrequencyFactor(22)
        .build())
    .active(ActiveEnum.ENUM_TRUE)
    .build();
```

