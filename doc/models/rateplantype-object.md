
# Rateplantype Object

## Structure

`RateplantypeObject`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `RatePlanGroupDescription` | `String` | Optional | - | String getRatePlanGroupDescription() | setRatePlanGroupDescription(String ratePlanGroupDescription) |
| `RatePlanType` | `String` | Optional | - | String getRatePlanType() | setRatePlanType(String ratePlanType) |
| `RatePlan` | [`List<Rateplantype2>`](../../doc/models/rateplantype-2.md) | Optional | An array of rateplan names | List<Rateplantype2> getRatePlan() | setRatePlan(List<Rateplantype2> ratePlan) |

## Example

```java
import com.verizon.thingspace.models.Rateplantype2;
import com.verizon.thingspace.models.RateplantypeObject;
import java.util.Arrays;

RateplantypeObject rateplantypeObject = new RateplantypeObject.Builder()
    .ratePlanGroupDescription("AGS Description_73")
    .ratePlanType("ratePlanType2")
    .ratePlan(Arrays.asList(
        new Rateplantype2.Builder()
            .description("description2")
            .sizeKb("sizeKb2")
            .carrierRatePlanCode("carrierRatePlanCode8")
            .zeroDollarBilling(false)
            .promotionOffered(false)
            .build(),
        new Rateplantype2.Builder()
            .description("description2")
            .sizeKb("sizeKb2")
            .carrierRatePlanCode("carrierRatePlanCode8")
            .zeroDollarBilling(false)
            .promotionOffered(false)
            .build()
    ))
    .build();
```

