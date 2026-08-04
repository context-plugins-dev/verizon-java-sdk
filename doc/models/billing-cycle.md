
# Billing Cycle

## Structure

`BillingCycle`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Year` | `String` | Optional | - | String getYear() | setYear(String year) |
| `Month` | `String` | Optional | - | String getMonth() | setMonth(String month) |

## Example

```java
import com.verizon.thingspace.models.BillingCycle;

BillingCycle billingCycle = new BillingCycle.Builder()
    .year("2020")
    .month("3")
    .build();
```

