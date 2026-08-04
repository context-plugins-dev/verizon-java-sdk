
# Rate Plan Group

## Structure

`RatePlanGroup`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `RatePlanGroupDescription` | `String` | Optional | - | String getRatePlanGroupDescription() | setRatePlanGroupDescription(String ratePlanGroupDescription) |
| `RatePlanType` | `Object` | Optional | - | Object getRatePlanType() | setRatePlanType(Object ratePlanType) |
| `RatePlan` | [`List<Rateplantype2>`](../../doc/models/rateplantype-2.md) | Optional | An array of rateplan names | List<Rateplantype2> getRatePlan() | setRatePlan(List<Rateplantype2> ratePlan) |
| `Description` | `String` | Optional | - | String getDescription() | setDescription(String description) |
| `SizeKb` | `String` | Optional | - | String getSizeKb() | setSizeKb(String sizeKb) |
| `CarrierRatePlanCode` | `String` | Optional | - | String getCarrierRatePlanCode() | setCarrierRatePlanCode(String carrierRatePlanCode) |
| `ZeroDollarBilling` | `Boolean` | Optional | - | Boolean getZeroDollarBilling() | setZeroDollarBilling(Boolean zeroDollarBilling) |
| `PromotionOffered` | `Boolean` | Optional | - | Boolean getPromotionOffered() | setPromotionOffered(Boolean promotionOffered) |
| `PromotionDays` | `Integer` | Optional | - | Integer getPromotionDays() | setPromotionDays(Integer promotionDays) |
| `Account` | [`List<Accountid>`](../../doc/models/accountid.md) | Optional | Account information | List<Accountid> getAccount() | setAccount(List<Accountid> account) |

## Example

```java
import com.verizon.thingspace.ApiHelper;
import com.verizon.thingspace.models.RatePlanGroup;
import com.verizon.thingspace.models.Rateplantype2;
import java.io.IOException;
import java.util.Arrays;

RatePlanGroup ratePlanGroup = new RatePlanGroup.Builder()
    .ratePlanGroupDescription("AGS Description_73")
    .ratePlanType(ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
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
            .build(),
        new Rateplantype2.Builder()
            .description("description2")
            .sizeKb("sizeKb2")
            .carrierRatePlanCode("carrierRatePlanCode8")
            .zeroDollarBilling(false)
            .promotionOffered(false)
            .build()
    ))
    .description("PlanDescription 2")
    .sizeKb("1048576")
    .carrierRatePlanCode("Service plan code value")
    .zeroDollarBilling(false)
    .promotionOffered(false)
    .promotionDays(-2147483648)
    .build();
```

