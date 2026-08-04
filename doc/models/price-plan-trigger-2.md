
# Price Plan Trigger 2

## Structure

`PricePlanTrigger2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountShare` | [`AccountShareFilterCriteria`](../../doc/models/account-share-filter-criteria.md) | Optional | - | AccountShareFilterCriteria getAccountShare() | setAccountShare(AccountShareFilterCriteria accountShare) |
| `Condition` | [`PricePlanTrigger2Condition`](../../doc/models/containers/price-plan-trigger-2-condition.md) | Optional | This is a container for any-of cases. | PricePlanTrigger2Condition getCondition() | setCondition(PricePlanTrigger2Condition condition) |
| `ChangePlan` | `Boolean` | Optional | a flag to set if the trigger changes service plans, true, or not, false | Boolean getChangePlan() | setChangePlan(Boolean changePlan) |
| `ChangePlanDetails` | [`ChangePlanDetails`](../../doc/models/change-plan-details.md) | Optional | The service plan code to switch to | ChangePlanDetails getChangePlanDetails() | setChangePlanDetails(ChangePlanDetails changePlanDetails) |
| `PayAsYouGo` | [`PayAsYouGoFilterCriteria`](../../doc/models/pay-as-you-go-filter-criteria.md) | Optional | - | PayAsYouGoFilterCriteria getPayAsYouGo() | setPayAsYouGo(PayAsYouGoFilterCriteria payAsYouGo) |
| `Action` | [`Actionobject`](../../doc/models/actionobject.md) | Optional | - | Actionobject getAction() | setAction(Actionobject action) |
| `StandAlone` | [`FiltercriteriaObjectCall`](../../doc/models/filtercriteria-object-call.md) | Optional | - | FiltercriteriaObjectCall getStandAlone() | setStandAlone(FiltercriteriaObjectCall standAlone) |

## Example

```java
import com.verizon.thingspace.models.AccountShareFilterCriteria;
import com.verizon.thingspace.models.AccountShareFilterCriteria1;
import com.verizon.thingspace.models.ChangePlanDetails;
import com.verizon.thingspace.models.ConditionTypeEnum;
import com.verizon.thingspace.models.PayAsYouGoFilterCriteria;
import com.verizon.thingspace.models.PayAsYouGoFilterCriteria1;
import com.verizon.thingspace.models.PricePlanTrigger2;
import com.verizon.thingspace.models.containers.PricePlanTrigger2Condition;
import java.util.Arrays;

PricePlanTrigger2 pricePlanTrigger2 = new PricePlanTrigger2.Builder()
    .accountShare(new AccountShareFilterCriteria.Builder()
        .filterCriteria(new AccountShareFilterCriteria1.Builder()
            .carrierServicePlanCode("carrierServicePlanCode4")
            .accountNameList(Arrays.asList(
                "accountNameList7",
                "accountNameList8"
            ))
            .build())
        .build())
    .condition(PricePlanTrigger2Condition.fromConditionType(
        ConditionTypeEnum.USAGEALLOWANCE
    ))
    .changePlan(true)
    .changePlanDetails(new ChangePlanDetails.Builder()
        .toCarrierServicePlanCode("toCarrierServicePlanCode2")
        .build())
    .payAsYouGo(new PayAsYouGoFilterCriteria.Builder()
        .filterCriteria(new PayAsYouGoFilterCriteria1.Builder()
            .carrierServicePlanCode("carrierServicePlanCode4")
            .accountNameList(Arrays.asList(
                "accountNameList7",
                "accountNameList8"
            ))
            .build())
        .build())
    .build();
```

