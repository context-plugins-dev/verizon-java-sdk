
# Account Group Share Filter Criteria

## Structure

`AccountGroupShareFilterCriteria`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `FilterCriteria` | [`AccountGroupShareFilter`](../../doc/models/account-group-share-filter.md) | Optional | - | AccountGroupShareFilter getFilterCriteria() | setFilterCriteria(AccountGroupShareFilter filterCriteria) |
| `Condition` | [`AccountGroupShareCondition`](../../doc/models/account-group-share-condition.md) | Optional | - | AccountGroupShareCondition getCondition() | setCondition(AccountGroupShareCondition condition) |
| `Action` | [`AccountGroupShareAction`](../../doc/models/account-group-share-action.md) | Optional | - | AccountGroupShareAction getAction() | setAction(AccountGroupShareAction action) |

## Example

```java
import com.verizon.thingspace.models.AccountGroupShareAction;
import com.verizon.thingspace.models.AccountGroupShareCondition;
import com.verizon.thingspace.models.AccountGroupShareFilter;
import com.verizon.thingspace.models.AccountGroupShareFilterCriteria;
import com.verizon.thingspace.models.AllowanceThreshold;
import com.verizon.thingspace.models.Carriercode1;
import com.verizon.thingspace.models.ConditionActionEnum;
import com.verizon.thingspace.models.Notify;
import com.verizon.thingspace.models.containers.NotifyThreshold;
import java.util.Arrays;

AccountGroupShareFilterCriteria accountGroupShareFilterCriteria = new AccountGroupShareFilterCriteria.Builder()
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
    .build();
```

