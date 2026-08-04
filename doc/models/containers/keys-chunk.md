
# Keys Chunk

## Class Name

`KeysChunk`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`KeyServicePlan`](../../../doc/models/key-service-plan.md) | KeysChunk.fromKeyServicePlan(KeyServicePlan keyServicePlan) |
| [`KeyDataPercentage50`](../../../doc/models/key-data-percentage-50.md) | KeysChunk.fromKeyDataPercentage50(KeyDataPercentage50 keyDataPercentage50) |
| [`KeysmsPercentage50`](../../../doc/models/keysms-percentage-50.md) | KeysChunk.fromKeysmsPercentage50(KeysmsPercentage50 keysmsPercentage50) |
| [`NoOfDaysB4PromoExp`](../../../doc/models/no-of-days-b4-promo-exp.md) | KeysChunk.fromNoOfDaysB4PromoExp(NoOfDaysB4PromoExp noOfDaysB4PromoExp) |
| [`EnablePromoExp`](../../../doc/models/enable-promo-exp.md) | KeysChunk.fromEnablePromoExp(EnablePromoExp enablePromoExp) |

## KeyServicePlan

### Initialization Code

#### Example

```java
KeysChunk.fromKeyServicePlan(
        new KeyServicePlan.Builder()
            .key("ServicePlan")
            .build()
    )
```

## KeyDataPercentage50

### Initialization Code

#### Example

```java
KeysChunk.fromKeyDataPercentage50(
        new KeyDataPercentage50.Builder()
            .key("DataPercentage50")
            .value(false)
            .build()
    )
```

## KeysmsPercentage50

### Initialization Code

#### Example

```java
KeysChunk.fromKeysmsPercentage50(
        new KeysmsPercentage50.Builder()
            .key("SmsPercentage50")
            .value(false)
            .build()
    )
```

## NoOfDaysB4PromoExp

### Initialization Code

#### Example

```java
KeysChunk.fromNoOfDaysB4PromoExp(
        new NoOfDaysB4PromoExp.Builder()
            .key("NoOfDaysB4PromoExp")
            .value(5)
            .build()
    )
```

## EnablePromoExp

### Initialization Code

#### Example

```java
KeysChunk.fromEnablePromoExp(
        new EnablePromoExp.Builder()
            .key("EnablePromoExp")
            .value(true)
            .build()
    )
```

