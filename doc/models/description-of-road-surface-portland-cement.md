
# Description of Road Surface Portland Cement

## Structure

`DescriptionOfRoadSurfacePortlandCement`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `PortlandCement` | [`PortlandCement`](../../doc/models/portland-cement.md) | Required | Indicates the surface of the roadway is portland cement. | PortlandCement getPortlandCement() | setPortlandCement(PortlandCement portlandCement) |

## Example

```java
import com.verizon.thingspace.models.DescriptionOfRoadSurfacePortlandCement;
import com.verizon.thingspace.models.PortlandCement;
import com.verizon.thingspace.models.Type6Enum;

DescriptionOfRoadSurfacePortlandCement descriptionOfRoadSurfacePortlandCement = new DescriptionOfRoadSurfacePortlandCement.Builder(
    new PortlandCement.Builder()
        .type(Type6Enum.TRAVELED)
        .build()
)
.build();
```

