
# Account Share Filter Criteria

## Structure

`AccountShareFilterCriteria`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `FilterCriteria` | [`AccountShareFilterCriteria1`](../../doc/models/account-share-filter-criteria-1.md) | Optional | - | AccountShareFilterCriteria1 getFilterCriteria() | setFilterCriteria(AccountShareFilterCriteria1 filterCriteria) |

## Example

```java
import com.verizon.thingspace.models.AccountShareFilterCriteria;
import com.verizon.thingspace.models.AccountShareFilterCriteria1;
import java.util.Arrays;

AccountShareFilterCriteria accountShareFilterCriteria = new AccountShareFilterCriteria.Builder()
    .filterCriteria(new AccountShareFilterCriteria1.Builder()
        .carrierServicePlanCode("carrierServicePlanCode4")
        .accountNameList(Arrays.asList(
            "accountNameList7",
            "accountNameList8"
        ))
        .build())
    .build();
```

