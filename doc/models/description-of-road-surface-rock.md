
# Description of Road Surface Rock

## Structure

`DescriptionOfRoadSurfaceRock`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Rock` | [`Rock`](../../doc/models/rock.md) | Required | Indicates the surface of the roadway is rock. | Rock getRock() | setRock(Rock rock) |

## Example

```java
import com.verizon.thingspace.models.DescriptionOfRoadSurfaceRock;
import com.verizon.thingspace.models.Rock;
import com.verizon.thingspace.models.Type11Enum;

DescriptionOfRoadSurfaceRock descriptionOfRoadSurfaceRock = new DescriptionOfRoadSurfaceRock.Builder(
    new Rock.Builder()
        .type(Type11Enum.CRUSHED)
        .build()
)
.build();
```

