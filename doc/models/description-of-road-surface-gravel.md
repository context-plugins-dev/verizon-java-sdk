
# Description of Road Surface Gravel

## Structure

`DescriptionOfRoadSurfaceGravel`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Gravel` | [`Gravel`](../../doc/models/gravel.md) | Required | Indicates the surface of the roadway is gravel. | Gravel getGravel() | setGravel(Gravel gravel) |

## Example

```java
import com.verizon.thingspace.models.DescriptionOfRoadSurfaceGravel;
import com.verizon.thingspace.models.Gravel;
import com.verizon.thingspace.models.Type8Enum;

DescriptionOfRoadSurfaceGravel descriptionOfRoadSurfaceGravel = new DescriptionOfRoadSurfaceGravel.Builder(
    new Gravel.Builder()
        .type(Type8Enum.PACKEDOILED)
        .build()
)
.build();
```

