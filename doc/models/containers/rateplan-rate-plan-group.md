
# Rateplan Rate Plan Group

## Class Name

`RateplanRatePlanGroup`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`RateplantypeObject`](../../../doc/models/rateplantype-object.md) | RateplanRatePlanGroup.fromRateplantypeObject(RateplantypeObject rateplantypeObject) |
| [`Rateplantype2`](../../../doc/models/rateplantype-2.md) | RateplanRatePlanGroup.fromRateplantype2(Rateplantype2 rateplantype2) |

## RateplantypeObject

### Initialization Code

#### Example

```java
RateplanRatePlanGroup.fromRateplantypeObject(
        new RateplantypeObject.Builder()
            .ratePlanGroupDescription("AGS Description_73")
            .build()
    )
```

## Rateplantype2

### Initialization Code

#### Example

```java
RateplanRatePlanGroup.fromRateplantype2(
        new Rateplantype2.Builder()
            .description("PlanDescription 2")
            .sizeKb("1048576")
            .carrierRatePlanCode("Service plan code value")
            .zeroDollarBilling(false)
            .promotionOffered(false)
            .promotionDays(-2147483648)
            .build()
    )
```

