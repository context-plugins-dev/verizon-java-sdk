
# Price Plan Trigger

## Structure

`PricePlanTrigger`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `StandAlone` | [`FiltercriteriaObjectCall`](../../doc/models/filtercriteria-object-call.md) | Optional | - | FiltercriteriaObjectCall getStandAlone() | setStandAlone(FiltercriteriaObjectCall standAlone) |
| `Condition` | [`PricePlanTriggerCondition`](../../doc/models/containers/price-plan-trigger-condition.md) | Optional | This is a container for any-of cases. | PricePlanTriggerCondition getCondition() | setCondition(PricePlanTriggerCondition condition) |
| `Action` | [`Actionobject`](../../doc/models/actionobject.md) | Optional | - | Actionobject getAction() | setAction(Actionobject action) |

## Example

```java
import com.verizon.thingspace.models.Actionobject;
import com.verizon.thingspace.models.ChangePlanDetails;
import com.verizon.thingspace.models.ConditionTypeEnum;
import com.verizon.thingspace.models.FilterCriteria1;
import com.verizon.thingspace.models.FiltercriteriaObjectCall;
import com.verizon.thingspace.models.PricePlanTrigger;
import com.verizon.thingspace.models.Suspenddetailsobject;
import com.verizon.thingspace.models.ThresholdUnitEnum;
import com.verizon.thingspace.models.containers.PricePlanTriggerCondition;
import java.util.Arrays;

PricePlanTrigger pricePlanTrigger = new PricePlanTrigger.Builder()
    .standAlone(new FiltercriteriaObjectCall.Builder()
        .filterCriteria(new FilterCriteria1.Builder()
            .carrierServicePlanCode("carrierServicePlanCode4")
            .accountNameList(Arrays.asList(
                "accountNameList7",
                "accountNameList8"
            ))
            .build())
        .build())
    .condition(PricePlanTriggerCondition.fromConditionType(
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
    .build();
```

