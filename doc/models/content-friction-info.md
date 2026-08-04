
# Content Friction Info

## Structure

`ContentFrictionInfo`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `FrictionInfo` | [`FrictionInformation`](../../doc/models/friction-information.md) | Required | - | FrictionInformation getFrictionInfo() | setFrictionInfo(FrictionInformation frictionInfo) |

## Example

```java
import com.verizon.thingspace.models.ContentFrictionInfo;
import com.verizon.thingspace.models.DescriptionOfRoadSurfacePortlandCement;
import com.verizon.thingspace.models.FrictionInformation;
import com.verizon.thingspace.models.PortlandCement;
import com.verizon.thingspace.models.Type6Enum;
import com.verizon.thingspace.models.containers.DescriptionOfRoadSurface;

ContentFrictionInfo contentFrictionInfo = new ContentFrictionInfo.Builder(
    new FrictionInformation.Builder(
        DescriptionOfRoadSurface.fromDescriptionOfRoadSurfacePortlandCement(
            new DescriptionOfRoadSurfacePortlandCement.Builder(
                new PortlandCement.Builder()
                    .type(Type6Enum.TRAVELED)
                    .build()
            )
            .build()
        )
    )
    .build()
)
.build();
```

