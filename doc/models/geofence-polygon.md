
# Geofence Polygon

GeoJSON Polygon geofence object.

## Structure

`GeofencePolygon`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | [`ETXMAPMessageGeofenceGeometryEnum`](../../doc/models/etxmap-message-geofence-geometry-enum.md) | Optional | Type of the GeoJSON geometry, must be 'Polygon'. | ETXMAPMessageGeofenceGeometryEnum getType() | setType(ETXMAPMessageGeofenceGeometryEnum type) |
| `Coordinates` | `List<List<Double>>` | Optional | Coordinates of the GeoJSON polygon.<br>Rules for a valid GeoJSON Polygon:<br><br>- Must contain between 4 and 50 points.<br>- Must be an array of linear rings (arrays of positions).<br>- The first linear ring represents the outer boundary; subsequent rings would represent holes. Holes are not supported, so only one linear ring should be defined in a polygon.<br>- Each linear ring must have at least 4 positions, and the first and last positions must be identical to close the polygon ring.<br>- A linear ring must follow the right-hand rule with respect to the area it bounds: exterior rings (outer boundery) are counterclockwise.<br>- Each position is an array of two numbers: [longitude, latitude].<br>- Longitude and latitude values must be in decimal degrees.<br>- Longitude must be ranging from -180 to 180.<br>- Latitude must be ranging from -90 to 90.<br>- The polygon must not self-intersect.<br><br>**Constraints**: *Minimum Items*: `4`, *Maximum Items*: `50` | List<List<Double>> getCoordinates() | setCoordinates(List<List<Double>> coordinates) |

## Example

```java
import com.verizon.thingspace.models.ETXMAPMessageGeofenceGeometryEnum;
import com.verizon.thingspace.models.GeofencePolygon;
import java.util.Arrays;

GeofencePolygon geofencePolygon = new GeofencePolygon.Builder()
    .type(ETXMAPMessageGeofenceGeometryEnum.POLYGON)
    .coordinates(Arrays.asList(
        Arrays.asList(
            -77.479395D,
            38.990773D
        ),
        Arrays.asList(
            -77.114566D,
            38.99944D
        ),
        Arrays.asList(
            -77.100228D,
            38.817204D
        ),
        Arrays.asList(
            -77.418059D,
            38.827754D
        ),
        Arrays.asList(
            -77.479395D,
            38.990773D
        )
    ))
    .build();
```

