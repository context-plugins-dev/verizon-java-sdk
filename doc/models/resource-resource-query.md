
# Resource Resource Query

## Structure

`ResourceResourceQuery`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Filter` | [`Devicepropertyfilter`](../../doc/models/devicepropertyfilter.md) | Optional | - | Devicepropertyfilter getFilter() | setFilter(Devicepropertyfilter filter) |

## Example

```java
import com.verizon.thingspace.models.Devicepropertyfilter;
import com.verizon.thingspace.models.Devicepropertyselection;
import com.verizon.thingspace.models.ResourceResourceQuery;

ResourceResourceQuery resourceResourceQuery = new ResourceResourceQuery.Builder()
    .filter(new Devicepropertyfilter.Builder()
        .selection(new Devicepropertyselection.Builder()
            .modelid("modelid0")
            .build())
        .querytotalcount(false)
        .build())
    .build();
```

