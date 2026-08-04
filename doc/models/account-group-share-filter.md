
# Account Group Share Filter

## Structure

`AccountGroupShareFilter`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `RatePlanGroupId` | `Integer` | Optional | - | Integer getRatePlanGroupId() | setRatePlanGroupId(Integer ratePlanGroupId) |

## Example

```java
import com.verizon.thingspace.models.AccountGroupShareFilter;

AccountGroupShareFilter accountGroupShareFilter = new AccountGroupShareFilter.Builder()
    .ratePlanGroupId(73)
    .build();
```

