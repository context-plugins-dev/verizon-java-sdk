
# Account Group Share Object

## Structure

`AccountGroupShareObject`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountGroupShare` | [`AccountGroupShareIndividual1`](../../doc/models/account-group-share-individual-1.md) | Optional | - | AccountGroupShareIndividual1 getAccountGroupShare() | setAccountGroupShare(AccountGroupShareIndividual1 accountGroupShare) |

## Example

```java
import com.verizon.thingspace.models.AccountGroupShareAction;
import com.verizon.thingspace.models.AccountGroupShareCondition;
import com.verizon.thingspace.models.AccountGroupShareFilter;
import com.verizon.thingspace.models.AccountGroupShareFilterCriteria;
import com.verizon.thingspace.models.AccountGroupShareIndividual1;
import com.verizon.thingspace.models.AccountGroupShareObject;
import com.verizon.thingspace.models.AllowanceThreshold;
import com.verizon.thingspace.models.Carriercode1;
import com.verizon.thingspace.models.ConditionActionEnum;
import com.verizon.thingspace.models.Notify;
import com.verizon.thingspace.models.containers.NotifyThreshold;
import java.util.Arrays;

AccountGroupShareObject accountGroupShareObject = new AccountGroupShareObject.Builder()
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
    .build();
```

