
# Account Group Share Action

## Structure

`AccountGroupShareAction`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Notify` | [`Notify`](../../doc/models/notify.md) | Optional | - | Notify getNotify() | setNotify(Notify notify) |

## Example

```java
import com.verizon.thingspace.models.AccountGroupShareAction;
import com.verizon.thingspace.models.AllowanceThreshold;
import com.verizon.thingspace.models.Carriercode1;
import com.verizon.thingspace.models.Notify;
import com.verizon.thingspace.models.containers.NotifyThreshold;
import java.util.Arrays;

AccountGroupShareAction accountGroupShareAction = new AccountGroupShareAction.Builder()
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
    .build();
```

