
# Carriercode 1

## Structure

`Carriercode1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CarrierCode` | `String` | Optional | - | String getCarrierCode() | setCarrierCode(String carrierCode) |
| `Percentage` | [`AllowanceThreshold`](../../doc/models/allowance-threshold.md) | Optional | - | AllowanceThreshold getPercentage() | setPercentage(AllowanceThreshold percentage) |

## Example

```java
import com.verizon.thingspace.models.AllowanceThreshold;
import com.verizon.thingspace.models.Carriercode1;

Carriercode1 carriercode1 = new Carriercode1.Builder()
    .carrierCode("Carrier identifier code 1")
    .percentage(new AllowanceThreshold.Builder()
        .percentage50(false)
        .percentage75(false)
        .percentage90(false)
        .percentage100(false)
        .build())
    .build();
```

