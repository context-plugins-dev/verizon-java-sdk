
# Account Share Price Plan Trigger

## Structure

`AccountSharePricePlanTrigger`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountShare` | [`AccountShareFilterCriteria`](../../doc/models/account-share-filter-criteria.md) | Optional | - | AccountShareFilterCriteria getAccountShare() | setAccountShare(AccountShareFilterCriteria accountShare) |
| `Condition` | [`AccountSharePricePlanTriggerCondition`](../../doc/models/containers/account-share-price-plan-trigger-condition.md) | Optional | This is a container for any-of cases. | AccountSharePricePlanTriggerCondition getCondition() | setCondition(AccountSharePricePlanTriggerCondition condition) |
| `ChangePlan` | `Boolean` | Optional | a flag to set if the trigger changes service plans, true, or not, false | Boolean getChangePlan() | setChangePlan(Boolean changePlan) |
| `ChangePlanDetails` | [`ChangePlanDetails`](../../doc/models/change-plan-details.md) | Optional | The service plan code to switch to | ChangePlanDetails getChangePlanDetails() | setChangePlanDetails(ChangePlanDetails changePlanDetails) |

## Example

```java
import com.verizon.thingspace.models.AccountShareFilterCriteria;
import com.verizon.thingspace.models.AccountShareFilterCriteria1;
import com.verizon.thingspace.models.AccountSharePricePlanTrigger;
import com.verizon.thingspace.models.ChangePlanDetails;
import com.verizon.thingspace.models.ConditionTypeEnum;
import com.verizon.thingspace.models.containers.AccountSharePricePlanTriggerCondition;
import java.util.Arrays;

AccountSharePricePlanTrigger accountSharePricePlanTrigger = new AccountSharePricePlanTrigger.Builder()
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
        ConditionTypeEnum.USAGEALLOWANCE
    ))
    .changePlan(true)
    .changePlanDetails(new ChangePlanDetails.Builder()
        .toCarrierServicePlanCode("toCarrierServicePlanCode2")
        .build())
    .build();
```

