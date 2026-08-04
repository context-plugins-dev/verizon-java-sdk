
# Description of Road Surface Snow

## Structure

`DescriptionOfRoadSurfaceSnow`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Snow` | [`Snow`](../../doc/models/snow.md) | Required | Indicates the surface of the roadway is snow. | Snow getSnow() | setSnow(Snow snow) |

## Example

```java
import com.verizon.thingspace.models.DescriptionOfRoadSurfaceSnow;
import com.verizon.thingspace.models.Snow;
import com.verizon.thingspace.models.Type13Enum;

DescriptionOfRoadSurfaceSnow descriptionOfRoadSurfaceSnow = new DescriptionOfRoadSurfaceSnow.Builder(
    new Snow.Builder()
        .type(Type13Enum.PACKED)
        .build()
)
.build();
```

