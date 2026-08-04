
# Pay as You Go Filter Criteria

## Structure

`PayAsYouGoFilterCriteria`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `FilterCriteria` | [`PayAsYouGoFilterCriteria1`](../../doc/models/pay-as-you-go-filter-criteria-1.md) | Optional | - | PayAsYouGoFilterCriteria1 getFilterCriteria() | setFilterCriteria(PayAsYouGoFilterCriteria1 filterCriteria) |

## Example

```java
import com.verizon.thingspace.models.PayAsYouGoFilterCriteria;
import com.verizon.thingspace.models.PayAsYouGoFilterCriteria1;
import java.util.Arrays;

PayAsYouGoFilterCriteria payAsYouGoFilterCriteria = new PayAsYouGoFilterCriteria.Builder()
    .filterCriteria(new PayAsYouGoFilterCriteria1.Builder()
        .carrierServicePlanCode("carrierServicePlanCode4")
        .accountNameList(Arrays.asList(
            "accountNameList7",
            "accountNameList8"
        ))
        .build())
    .build();
```

