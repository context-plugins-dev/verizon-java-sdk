
# M5 G Bi Carrier Information

## Structure

`M5gBiCarrierInformation`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CarrierName` | `String` | Optional | - | String getCarrierName() | setCarrierName(String carrierName) |

## Example

```java
import com.verizon.thingspace.models.M5gBiCarrierInformation;

M5gBiCarrierInformation m5gBiCarrierInformation = new M5gBiCarrierInformation.Builder()
    .carrierName("Verizon Wireless")
    .build();
```

