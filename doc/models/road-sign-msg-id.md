
# Road Sign Msg Id

Message ID referencing a road sign location.

## Structure

`RoadSignMsgId`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `RoadSignID` | [`RoadSignID`](../../doc/models/road-sign-id.md) | Required | It provide a precise location of one or more roadside signs. | RoadSignID getRoadSignID() | setRoadSignID(RoadSignID roadSignID) |

## Example

```java
import com.verizon.thingspace.models.RoadSignID;
import com.verizon.thingspace.models.RoadSignMsgId;
import com.verizon.thingspace.models.RoadSignPosition;

RoadSignMsgId roadSignMsgId = new RoadSignMsgId.Builder(
    new RoadSignID.Builder(
        new RoadSignPosition.Builder(
            14,
            172
        )
        .build(),
        "1101"
    )
    .build()
)
.build();
```

