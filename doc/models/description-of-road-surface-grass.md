
# Description of Road Surface Grass

## Structure

`DescriptionOfRoadSurfaceGrass`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Grass` | [`Grass`](../../doc/models/grass.md) | Required | Indicates the surface of the roadway is grass. | Grass getGrass() | setGrass(Grass grass) |

## Example

```java
import com.verizon.thingspace.models.DescriptionOfRoadSurfaceGrass;
import com.verizon.thingspace.models.Grass;
import com.verizon.thingspace.models.Type9Enum;

DescriptionOfRoadSurfaceGrass descriptionOfRoadSurfaceGrass = new DescriptionOfRoadSurfaceGrass.Builder(
    new Grass.Builder()
        .type(Type9Enum.LESSTHAN30MPH)
        .build()
)
.build();
```

