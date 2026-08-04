
# Node Offset Point LL

The NodeOffsetPointLL data frame presents a structure to hold 64 bits sized data frames for a single node geometry path. Nodes are described in terms of latitude and longitude.

## Structure

`NodeOffsetPointLL`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NodeLatLon` | [`NodeLLmD64b`](../../doc/models/node-l-lm-d64-b.md) | Required | A 64-bit node type with lat-long values expressed in standard SAE 1/10th of a microdegree. | NodeLLmD64b getNodeLatLon() | setNodeLatLon(NodeLLmD64b nodeLatLon) |

## Example

```java
import com.verizon.thingspace.models.NodeLLmD64b;
import com.verizon.thingspace.models.NodeOffsetPointLL;

NodeOffsetPointLL nodeOffsetPointLL = new NodeOffsetPointLL.Builder(
    new NodeLLmD64b.Builder(
        40,
        10
    )
    .build()
)
.build();
```

