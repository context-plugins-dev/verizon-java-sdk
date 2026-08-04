
# Geographical Path

The data frame is used to support the cross-cutting need in many V2X messages to describe arbitrary spatial areas (polygons, boundary lines, and other basic shapes) required by various message types in a small message size.

## Structure

`GeographicalPath`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Description` | [`GeographicalPathDescription`](../../doc/models/geographical-path-description.md) | Optional | This data frame can describe a complex path of arbitrary size using node offset method (LL offsets). | GeographicalPathDescription getDescription() | setDescription(GeographicalPathDescription description) |
| `Direction` | `String` | Optional | OctetStrings are described as hexadecimal strings, where each octet is represented by two hexadecimal characters.<br><br>**Constraints**: *Pattern*: `^[0-9A-Fa-f]{4}$` | String getDirection() | setDirection(String direction) |

## Example

```java
import com.verizon.thingspace.models.GeographicalPath;
import com.verizon.thingspace.models.GeographicalPathDescription;
import com.verizon.thingspace.models.NodeLL;
import com.verizon.thingspace.models.NodeLLmD64b;
import com.verizon.thingspace.models.NodeListLL;
import com.verizon.thingspace.models.NodeOffsetPointLL;
import com.verizon.thingspace.models.Offset;
import com.verizon.thingspace.models.OffsetSystem;
import java.util.Arrays;

GeographicalPath geographicalPath = new GeographicalPath.Builder()
    .description(new GeographicalPathDescription.Builder(
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
                        .build(),
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
    .build())
    .direction("1101")
    .build();
```

