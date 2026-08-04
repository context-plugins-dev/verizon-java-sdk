
# Node LL

The NodeLL data frame presents a structure to hold data for a signal node point in a lane. Each selected node has a complete lat-long representation.

## Structure

`NodeLL`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Delta` | [`NodeOffsetPointLL`](../../doc/models/node-offset-point-ll.md) | Required | The NodeOffsetPointLL data frame presents a structure to hold 64 bits sized data frames for a single node geometry path. Nodes are described in terms of latitude and longitude. | NodeOffsetPointLL getDelta() | setDelta(NodeOffsetPointLL delta) |

## Example

```java
import com.verizon.thingspace.models.NodeLL;
import com.verizon.thingspace.models.NodeLLmD64b;
import com.verizon.thingspace.models.NodeOffsetPointLL;

NodeLL nodeLL = new NodeLL.Builder(
    new NodeOffsetPointLL.Builder(
        new NodeLLmD64b.Builder(
            40,
            10
        )
        .build()
    )
    .build()
)
.build();
```

