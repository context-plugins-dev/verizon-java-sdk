
# Offset System

The OffsetSystem data frame selects a sequence of node offsets described in the Lat-Long offset method.

## Structure

`OffsetSystem`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Offset` | [`Offset`](../../doc/models/offset.md) | Required | The sequence of node offsets then describes a path or polygon in the Lat-Long system. | Offset getOffset() | setOffset(Offset offset) |

## Example

```java
import com.verizon.thingspace.models.NodeLL;
import com.verizon.thingspace.models.NodeLLmD64b;
import com.verizon.thingspace.models.NodeListLL;
import com.verizon.thingspace.models.NodeOffsetPointLL;
import com.verizon.thingspace.models.Offset;
import com.verizon.thingspace.models.OffsetSystem;
import java.util.Arrays;

OffsetSystem offsetSystem = new OffsetSystem.Builder(
    new Offset.Builder(
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
    .build()
)
.build();
```

