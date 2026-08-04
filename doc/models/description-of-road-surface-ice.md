
# Description of Road Surface Ice

## Structure

`DescriptionOfRoadSurfaceIce`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Ice` | [`Ice`](../../doc/models/ice.md) | Required | Indicates the surface of the roadway is ice. | Ice getIce() | setIce(Ice ice) |

## Example

```java
import com.verizon.thingspace.models.DescriptionOfRoadSurfaceIce;
import com.verizon.thingspace.models.Ice;
import com.verizon.thingspace.models.Type12Enum;

DescriptionOfRoadSurfaceIce descriptionOfRoadSurfaceIce = new DescriptionOfRoadSurfaceIce.Builder(
    new Ice.Builder()
        .type(Type12Enum.SMOOTH)
        .build()
)
.build();
```

