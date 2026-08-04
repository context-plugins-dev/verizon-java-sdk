
# Polygon

A Polygon is a type of geometry that represents a collection of points that form a closed ring.

NOTE: This API only supports a single polygon in the Polygon geometry, so holes cannot be defines at this point. Support for hole will be added in future releases.

## Structure

`Polygon`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | [`Type3Enum`](../../doc/models/type-3-enum.md) | Required | - | Type3Enum getType() | setType(Type3Enum type) |
| `Coordinates` | `List<List<List<Double>>>` | Required | **Constraints**: *Minimum Items*: `1`, *Maximum Items*: `1`, `>= -180`, `<= 180` | List<List<List<Double>>> getCoordinates() | setCoordinates(List<List<List<Double>>> coordinates) |

## Example

```java
import com.verizon.thingspace.models.Polygon;
import com.verizon.thingspace.models.Type3Enum;
import java.util.Arrays;

Polygon polygon = new Polygon.Builder(
    Type3Enum.POLYGON,
    Arrays.asList(
        Arrays.asList(
            Arrays.asList(
                41.65D,
                41.66D
            ),
            Arrays.asList(
                41.65D,
                41.66D
            )
        ),
        Arrays.asList(
            Arrays.asList(
                41.65D,
                41.66D
            ),
            Arrays.asList(
                41.65D,
                41.66D
            )
        )
    )
)
.build();
```

