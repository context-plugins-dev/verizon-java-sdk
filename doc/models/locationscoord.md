
# Locationscoord

Location coordinates.

## Structure

`Locationscoord`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CoordinatesList` | [`List<Coordinates>`](../../doc/models/coordinates.md) | Optional | - | List<Coordinates> getCoordinatesList() | setCoordinatesList(List<Coordinates> coordinatesList) |

## Example

```java
import com.verizon.thingspace.models.Coordinates;
import com.verizon.thingspace.models.Locationscoord;
import java.util.Arrays;

Locationscoord locationscoord = new Locationscoord.Builder()
    .coordinatesList(Arrays.asList(
        new Coordinates.Builder()
            .latitude("latitude6")
            .longitude("longitude4")
            .build()
    ))
    .build();
```

