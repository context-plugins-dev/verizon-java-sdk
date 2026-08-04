
# Rateplan

## Structure

`Rateplan`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `RatePlanGroup` | [`List<RateplanRatePlanGroup>`](../../doc/models/containers/rateplan-rate-plan-group.md) | Optional | This is List of a container for any-of cases. | List<RateplanRatePlanGroup> getRatePlanGroup() | setRatePlanGroup(List<RateplanRatePlanGroup> ratePlanGroup) |

## Example

```java
import com.verizon.thingspace.models.Rateplan;
import com.verizon.thingspace.models.Rateplantype2;
import com.verizon.thingspace.models.RateplantypeObject;
import com.verizon.thingspace.models.containers.RateplanRatePlanGroup;
import java.util.Arrays;

Rateplan rateplan = new Rateplan.Builder()
    .ratePlanGroup(Arrays.asList(
        RateplanRatePlanGroup.fromRateplantypeObject(
            new RateplantypeObject.Builder()
                .ratePlanGroupDescription("ratePlanGroupDescription4")
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
                .build()
        ),
        RateplanRatePlanGroup.fromRateplantypeObject(
            new RateplantypeObject.Builder()
                .ratePlanGroupDescription("ratePlanGroupDescription4")
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
                .build()
        ),
        RateplanRatePlanGroup.fromRateplantypeObject(
            new RateplantypeObject.Builder()
                .ratePlanGroupDescription("ratePlanGroupDescription4")
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
                .build()
        )
    ))
    .build();
```

