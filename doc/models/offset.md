
# Offset

The sequence of node offsets then describes a path or polygon in the Lat-Long system.

## Structure

`Offset`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Ll` | [`NodeListLL`](../../doc/models/node-list-ll.md) | Required | The NodeListLL data structure provides the sequence of signed offset node point values for determining the latitude and longitude. Each LL point is referred to as a node point. | NodeListLL getLl() | setLl(NodeListLL ll) |

## Example

```java
import com.verizon.thingspace.models.NodeLL;
import com.verizon.thingspace.models.NodeLLmD64b;
import com.verizon.thingspace.models.NodeListLL;
import com.verizon.thingspace.models.NodeOffsetPointLL;
import com.verizon.thingspace.models.Offset;
import java.util.Arrays;

Offset offset = new Offset.Builder(
    new NodeListLL.Builder(
        Arrays.asList(
            new NodeLL.Builder(
                new NodeOffsetPointLL.Builder(
                    new NodeLLmD64b.Builder(
                        40,
                        10
                    )
                    .build()
                )
                .build()
            )
            .build()
        )
    )
    .build()
)
.build();
```

