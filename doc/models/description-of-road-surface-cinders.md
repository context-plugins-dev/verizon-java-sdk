
# Description of Road Surface Cinders

## Structure

`DescriptionOfRoadSurfaceCinders`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Cinders` | [`Cinders`](../../doc/models/cinders.md) | Required | Indicates the surface of the roadway is cinders. | Cinders getCinders() | setCinders(Cinders cinders) |

## Example

```java
import com.verizon.thingspace.models.Cinders;
import com.verizon.thingspace.models.DescriptionOfRoadSurfaceCinders;
import com.verizon.thingspace.models.Type10Enum;

DescriptionOfRoadSurfaceCinders descriptionOfRoadSurfaceCinders = new DescriptionOfRoadSurfaceCinders.Builder(
    new Cinders.Builder()
        .type(Type10Enum.PACKED)
        .build()
)
.build();
```

