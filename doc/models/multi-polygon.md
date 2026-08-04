
# Multi Polygon

A MultiPolygon is a type of geometry that represents a collection of Polygon geometries.

## Structure

`MultiPolygon`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | [`Type5Enum`](../../doc/models/type-5-enum.md) | Required | - | Type5Enum getType() | setType(Type5Enum type) |
| `Coordinates` | `List<List<List<List<Double>>>>` | Required | **Constraints**: *Minimum Items*: `1`, *Maximum Items*: `10`, `>= -180`, `<= 180` | List<List<List<List<Double>>>> getCoordinates() | setCoordinates(List<List<List<List<Double>>>> coordinates) |

## Example

```java
import com.verizon.thingspace.models.MultiPolygon;
import com.verizon.thingspace.models.Type5Enum;
import java.util.Arrays;

MultiPolygon multiPolygon = new MultiPolygon.Builder(
    Type5Enum.MULTIPOLYGON,
    Arrays.asList(
        Arrays.asList(
            Arrays.asList(
                Arrays.asList(
                    56.89D
                )
            )
        )
    )
)
.build();
```

