
# Road Sign ID

It provide a precise location of one or more roadside signs.

## Structure

`RoadSignID`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Position` | [`RoadSignPosition`](../../doc/models/road-sign-position.md) | Required | Precise location of a road sign in the WGS-84 coordinate system, from which short offsets may be used to create additional data using a flat earth projection centered on this location. | RoadSignPosition getPosition() | setPosition(RoadSignPosition position) |
| `ViewAngle` | `String` | Required | OctetStrings are described as hexadecimal strings, where each octet is represented by two hexadecimal characters.<br><br>**Constraints**: *Pattern*: `^[0-9A-Fa-f]{4}$` | String getViewAngle() | setViewAngle(String viewAngle) |

## Example

```java
import com.verizon.thingspace.models.RoadSignID;
import com.verizon.thingspace.models.RoadSignPosition;

RoadSignID roadSignID = new RoadSignID.Builder(
    new RoadSignPosition.Builder(
        14,
        172
    )
    .build(),
    "1101"
)
.build();
```

