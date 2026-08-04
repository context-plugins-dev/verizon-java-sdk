
# Pay as You Go Create Trigger Request

## Structure

`PayAsYouGoCreateTriggerRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `TriggerName` | `String` | Optional | The user defined name of the trigger | String getTriggerName() | setTriggerName(String triggerName) |
| `EcpdId` | `String` | Optional | The Enterprise Customer Profile Database ID | String getEcpdId() | setEcpdId(String ecpdId) |
| `TriggerCategory` | [`TriggerCategoryEnum`](../../doc/models/trigger-category-enum.md) | Optional | The type of trigger being created or modified | TriggerCategoryEnum getTriggerCategory() | setTriggerCategory(TriggerCategoryEnum triggerCategory) |
| `PricePlanTrigger` | [`PayAsYouGoPricePlanTrigger`](../../doc/models/pay-as-you-go-price-plan-trigger.md) | Optional | - | PayAsYouGoPricePlanTrigger getPricePlanTrigger() | setPricePlanTrigger(PayAsYouGoPricePlanTrigger pricePlanTrigger) |
| `Notification` | [`Notificationarray`](../../doc/models/notificationarray.md) | Optional | - | Notificationarray getNotification() | setNotification(Notificationarray notification) |
| `Active` | [`ActiveEnum`](../../doc/models/active-enum.md) | Optional | A flag to indicate of the trigger is active, true, or not, false | ActiveEnum getActive() | setActive(ActiveEnum active) |

## Example

```java
import com.verizon.thingspace.models.Actionobject;
import com.verizon.thingspace.models.ActiveEnum;
import com.verizon.thingspace.models.ChangePlanDetails;
import com.verizon.thingspace.models.ConditionTypeEnum;
import com.verizon.thingspace.models.Notificationarray;
import com.verizon.thingspace.models.PayAsYouGoCreateTriggerRequest;
import com.verizon.thingspace.models.PayAsYouGoFilterCriteria;
import com.verizon.thingspace.models.PayAsYouGoFilterCriteria1;
import com.verizon.thingspace.models.PayAsYouGoPricePlanTrigger;
import com.verizon.thingspace.models.Suspenddetailsobject;
import com.verizon.thingspace.models.ThresholdUnitEnum;
import com.verizon.thingspace.models.TriggerCategoryEnum;
import com.verizon.thingspace.models.containers.PayAsYouGoPricePlanTriggerCondition;
import java.util.Arrays;

PayAsYouGoCreateTriggerRequest payAsYouGoCreateTriggerRequest = new PayAsYouGoCreateTriggerRequest.Builder()
    .triggerName("name of the trigger")
    .ecpdId("Verizon profile ID")
    .triggerCategory(TriggerCategoryEnum.DEVICEGROUPUSAGE)
    .pricePlanTrigger(new PayAsYouGoPricePlanTrigger.Builder()
        .payAsYouGo(new PayAsYouGoFilterCriteria.Builder()
            .filterCriteria(new PayAsYouGoFilterCriteria1.Builder()
                .carrierServicePlanCode("carrierServicePlanCode4")
                .accountNameList(Arrays.asList(
                    "accountNameList7",
                    "accountNameList8"
                ))
                .build())
            .build())
        .condition(PayAsYouGoPricePlanTriggerCondition.fromConditionType(
            ConditionTypeEnum.AGING
        ))
        .action(new Actionobject.Builder()
            .suspend(false)
            .suspendDetails(new Suspenddetailsobject.Builder()
                .suspendFromAccounts(Arrays.asList(
                    "suspendFromAccounts7"
                ))
                .suspendDuration(152)
                .suspendOption("suspendOption2")
                .threshold(166)
                .thresholdUnit(ThresholdUnitEnum.GB)
                .build())
            .changePlan(false)
            .changePlanDetails(new ChangePlanDetails.Builder()
                .toCarrierServicePlanCode("toCarrierServicePlanCode2")
                .build())
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

