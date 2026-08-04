
# Geographical Path Description

This data frame can describe a complex path of arbitrary size using node offset method (LL offsets).

## Structure

`GeographicalPathDescription`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Path` | [`OffsetSystem`](../../doc/models/offset-system.md) | Required | The OffsetSystem data frame selects a sequence of node offsets described in the Lat-Long offset method. | OffsetSystem getPath() | setPath(OffsetSystem path) |

## Example

```java
import com.verizon.thingspace.models.GeographicalPathDescription;
import com.verizon.thingspace.models.NodeLL;
import com.verizon.thingspace.models.NodeLLmD64b;
import com.verizon.thingspace.models.NodeListLL;
import com.verizon.thingspace.models.NodeOffsetPointLL;
import com.verizon.thingspace.models.Offset;
import com.verizon.thingspace.models.OffsetSystem;
import java.util.Arrays;

GeographicalPathDescription geographicalPathDescription = new GeographicalPathDescription.Builder(
    new OffsetSystem.Builder(
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
    .build()
)
.build();
```

