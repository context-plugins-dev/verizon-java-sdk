
# Price Plan Trigger 1

## Structure

`PricePlanTrigger1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountGroupShare` | [`AccountGroupShareIndividual1`](../../doc/models/account-group-share-individual-1.md) | Optional | - | AccountGroupShareIndividual1 getAccountGroupShare() | setAccountGroupShare(AccountGroupShareIndividual1 accountGroupShare) |
| `AccountShare` | [`AccountShareFilterCriteria`](../../doc/models/account-share-filter-criteria.md) | Optional | - | AccountShareFilterCriteria getAccountShare() | setAccountShare(AccountShareFilterCriteria accountShare) |
| `Condition` | [`PricePlanTrigger1Condition`](../../doc/models/containers/price-plan-trigger-1-condition.md) | Optional | This is a container for any-of cases. | PricePlanTrigger1Condition getCondition() | setCondition(PricePlanTrigger1Condition condition) |
| `ChangePlan` | `Boolean` | Optional | a flag to set if the trigger changes service plans, true, or not, false | Boolean getChangePlan() | setChangePlan(Boolean changePlan) |
| `ChangePlanDetails` | [`ChangePlanDetails`](../../doc/models/change-plan-details.md) | Optional | The service plan code to switch to | ChangePlanDetails getChangePlanDetails() | setChangePlanDetails(ChangePlanDetails changePlanDetails) |
| `PayAsYouGo` | [`PayAsYouGoFilterCriteria`](../../doc/models/pay-as-you-go-filter-criteria.md) | Optional | - | PayAsYouGoFilterCriteria getPayAsYouGo() | setPayAsYouGo(PayAsYouGoFilterCriteria payAsYouGo) |
| `Action` | [`Actionobject`](../../doc/models/actionobject.md) | Optional | - | Actionobject getAction() | setAction(Actionobject action) |
| `StandAlone` | [`FiltercriteriaObjectCall`](../../doc/models/filtercriteria-object-call.md) | Optional | - | FiltercriteriaObjectCall getStandAlone() | setStandAlone(FiltercriteriaObjectCall standAlone) |

## Example

```java
import com.verizon.thingspace.models.AccountGroupShareAction;
import com.verizon.thingspace.models.AccountGroupShareCondition;
import com.verizon.thingspace.models.AccountGroupShareFilter;
import com.verizon.thingspace.models.AccountGroupShareFilterCriteria;
import com.verizon.thingspace.models.AccountGroupShareIndividual1;
import com.verizon.thingspace.models.AccountShareFilterCriteria;
import com.verizon.thingspace.models.AccountShareFilterCriteria1;
import com.verizon.thingspace.models.AllowanceThreshold;
import com.verizon.thingspace.models.Carriercode1;
import com.verizon.thingspace.models.ChangePlanDetails;
import com.verizon.thingspace.models.ConditionActionEnum;
import com.verizon.thingspace.models.ConditionTypeEnum;
import com.verizon.thingspace.models.Notify;
import com.verizon.thingspace.models.PricePlanTrigger1;
import com.verizon.thingspace.models.containers.NotifyThreshold;
import com.verizon.thingspace.models.containers.PricePlanTrigger1Condition;
import java.util.Arrays;

PricePlanTrigger1 pricePlanTrigger1 = new PricePlanTrigger1.Builder()
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
    .accountShare(new AccountShareFilterCriteria.Builder()
        .filterCriteria(new AccountShareFilterCriteria1.Builder()
            .carrierServicePlanCode("carrierServicePlanCode4")
            .accountNameList(Arrays.asList(
                "accountNameList7",
                "accountNameList8"
            ))
            .build())
        .build())
    .condition(PricePlanTrigger1Condition.fromConditionType(
        ConditionTypeEnum.AGING
    ))
    .changePlan(true)
    .changePlanDetails(new ChangePlanDetails.Builder()
        .toCarrierServicePlanCode("toCarrierServicePlanCode2")
        .build())
    .build();
```

