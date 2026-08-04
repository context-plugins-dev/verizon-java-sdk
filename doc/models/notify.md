
# Notify

## Structure

`Notify`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AlertType` | `String` | Optional | - | String getAlertType() | setAlertType(String alertType) |
| `Threshold` | [`List<NotifyThreshold>`](../../doc/models/containers/notify-threshold.md) | Optional | This is List of a container for any-of cases. | List<NotifyThreshold> getThreshold() | setThreshold(List<NotifyThreshold> threshold) |

## Example

```java
import com.verizon.thingspace.models.AllowanceThreshold;
import com.verizon.thingspace.models.Carriercode1;
import com.verizon.thingspace.models.Notify;
import com.verizon.thingspace.models.containers.NotifyThreshold;
import java.util.Arrays;

Notify notify = new Notify.Builder()
    .alertType("individualpriceplan")
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
    .build();
```

