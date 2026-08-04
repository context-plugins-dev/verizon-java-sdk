
# Pay as You Go Price Plan Trigger

## Structure

`PayAsYouGoPricePlanTrigger`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `PayAsYouGo` | [`PayAsYouGoFilterCriteria`](../../doc/models/pay-as-you-go-filter-criteria.md) | Optional | - | PayAsYouGoFilterCriteria getPayAsYouGo() | setPayAsYouGo(PayAsYouGoFilterCriteria payAsYouGo) |
| `Condition` | [`PayAsYouGoPricePlanTriggerCondition`](../../doc/models/containers/pay-as-you-go-price-plan-trigger-condition.md) | Optional | This is a container for any-of cases. | PayAsYouGoPricePlanTriggerCondition getCondition() | setCondition(PayAsYouGoPricePlanTriggerCondition condition) |
| `Action` | [`Actionobject`](../../doc/models/actionobject.md) | Optional | - | Actionobject getAction() | setAction(Actionobject action) |

## Example

```java
import com.verizon.thingspace.models.Actionobject;
import com.verizon.thingspace.models.ChangePlanDetails;
import com.verizon.thingspace.models.ConditionTypeEnum;
import com.verizon.thingspace.models.PayAsYouGoFilterCriteria;
import com.verizon.thingspace.models.PayAsYouGoFilterCriteria1;
import com.verizon.thingspace.models.PayAsYouGoPricePlanTrigger;
import com.verizon.thingspace.models.Suspenddetailsobject;
import com.verizon.thingspace.models.ThresholdUnitEnum;
import com.verizon.thingspace.models.containers.PayAsYouGoPricePlanTriggerCondition;
import java.util.Arrays;

PayAsYouGoPricePlanTrigger payAsYouGoPricePlanTrigger = new PayAsYouGoPricePlanTrigger.Builder()
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
        ConditionTypeEnum.INDIVIDUAL
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
    .build();
```

