
# Filtercriteria Object Call

## Structure

`FiltercriteriaObjectCall`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `FilterCriteria` | [`FilterCriteria1`](../../doc/models/filter-criteria-1.md) | Optional | - | FilterCriteria1 getFilterCriteria() | setFilterCriteria(FilterCriteria1 filterCriteria) |

## Example

```java
import com.verizon.thingspace.models.FilterCriteria1;
import com.verizon.thingspace.models.FiltercriteriaObjectCall;
import java.util.Arrays;

FiltercriteriaObjectCall filtercriteriaObjectCall = new FiltercriteriaObjectCall.Builder()
    .filterCriteria(new FilterCriteria1.Builder()
        .carrierServicePlanCode("carrierServicePlanCode4")
        .accountNameList(Arrays.asList(
            "accountNameList7",
            "accountNameList8"
        ))
        .build())
    .build();
```

