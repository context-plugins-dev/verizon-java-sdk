
# Friction Information

## Structure

`FrictionInformation`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `RoadSurfaceDescription` | [`DescriptionOfRoadSurface`](../../doc/models/containers/description-of-road-surface.md) | Required | Indicates the composition of the surface of the roadway for use in estimation of friction. | DescriptionOfRoadSurface getRoadSurfaceDescription() | setRoadSurfaceDescription(DescriptionOfRoadSurface roadSurfaceDescription) |

## Example

```java
import com.verizon.thingspace.models.DescriptionOfRoadSurfacePortlandCement;
import com.verizon.thingspace.models.FrictionInformation;
import com.verizon.thingspace.models.PortlandCement;
import com.verizon.thingspace.models.Type6Enum;
import com.verizon.thingspace.models.containers.DescriptionOfRoadSurface;

FrictionInformation frictionInformation = new FrictionInformation.Builder(
    DescriptionOfRoadSurface.fromDescriptionOfRoadSurfacePortlandCement(
        new DescriptionOfRoadSurfacePortlandCement.Builder(
            new PortlandCement.Builder()
                .type(Type6Enum.TRAVELED)
                .build()
        )
        .build()
    )
)
.build();
```

