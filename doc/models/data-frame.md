
# Data Frame

The data frame allows sending various advisory and road sign types of information to equipped devices.

## Structure

`DataFrame`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DoNotUse1` | `Integer` | Optional | Always set to 0 and carries no meaning. Legacy field maintained for backward compatibility.<br><br>**Default**: `0`<br><br>**Constraints**: `>= 0`, `<= 31` | Integer getDoNotUse1() | setDoNotUse1(Integer doNotUse1) |
| `FrameType` | [`FrameTypeEnum`](../../doc/models/frame-type-enum.md) | Required | The frameType data element provides the type of message to follow in the rest of the message frame structure. The following frame types are supported:<br><br>- unknown<br>- advisory<br>- roadSignage<br>- commercialSignage | FrameTypeEnum getFrameType() | setFrameType(FrameTypeEnum frameType) |
| `MsgId` | [`DataFrameMsgId`](../../doc/models/containers/data-frame-msg-id.md) | Required | This is a container for one-of cases. | DataFrameMsgId getMsgId() | setMsgId(DataFrameMsgId msgId) |
| `StartYear` | `Integer` | Optional | The V2X year consists of integer values from zero to 4095 representing the year according to the Gregorian calendar date system. The value of zero shall represent an unknown value.<br><br>**Constraints**: `>= 0`, `<= 4095` | Integer getStartYear() | setStartYear(Integer startYear) |
| `StartTime` | `int` | Required | Start time expresses the number of elapsed minutes of the current year in the time system being used (typically UTC time). The value 527040 shall be used for invalid.<br><br>**Constraints**: `>= 0`, `<= 527040` | int getStartTime() | setStartTime(int startTime) |
| `DurationTime` | `int` | Required | The duration, in units of whole minutes, that a object persists for. A value of 32000 means that the object persists forever. The range 0..32000 provides for about 22.2 days of maximum duration.<br><br>**Constraints**: `>= 0`, `<= 32000` | int getDurationTime() | setDurationTime(int durationTime) |
| `Priority` | `int` | Required | The relative importance of the sign, on a scale from zero (least important) to seven (most important).<br><br>**Constraints**: `>= 0`, `<= 7` | int getPriority() | setPriority(int priority) |
| `DoNotUse2` | `Integer` | Optional | Always set to 0 and carries no meaning. Legacy field maintained for backward compatibility.<br><br>**Default**: `0`<br><br>**Constraints**: `>= 0`, `<= 31` | Integer getDoNotUse2() | setDoNotUse2(Integer doNotUse2) |
| `Regions` | [`List<GeographicalPath>`](../../doc/models/geographical-path.md) | Required | The data frame is used to support the cross-cutting need in many V2X messages to describe arbitrary spatial areas (polygons, boundary lines, and other basic shapes) required by various message types in a small message size. This data frame can describe a complex path or region of arbitrary size using either one of the two supported node offset methods (XY offsets or LL offsets) or using simple geometric projections.<br><br>**Constraints**: *Minimum Items*: `1`, *Maximum Items*: `16` | List<GeographicalPath> getRegions() | setRegions(List<GeographicalPath> regions) |
| `DoNotUse3` | `Integer` | Optional | Always set to 0 and carries no meaning. Legacy field maintained for backward compatibility.<br><br>**Default**: `0`<br><br>**Constraints**: `>= 0`, `<= 31` | Integer getDoNotUse3() | setDoNotUse3(Integer doNotUse3) |
| `DoNotUse4` | `Integer` | Optional | Always set to 0 and carries no meaning. Legacy field maintained for backward compatibility.<br><br>**Default**: `0`<br><br>**Constraints**: `>= 0`, `<= 31` | Integer getDoNotUse4() | setDoNotUse4(Integer doNotUse4) |
| `Content` | [`DataFrameContent`](../../doc/models/containers/data-frame-content.md) | Required | This is a container for one-of cases. | DataFrameContent getContent() | setContent(DataFrameContent content) |
| `ContentNew` | [`DataFrameContentNew`](../../doc/models/containers/data-frame-content-new.md) | Optional | This is a container for one-of cases. | DataFrameContentNew getContentNew() | setContentNew(DataFrameContentNew contentNew) |

## Example

```java
import com.verizon.thingspace.models.AdvisoryContent;
import com.verizon.thingspace.models.DataFrame;
import com.verizon.thingspace.models.FrameTypeEnum;
import com.verizon.thingspace.models.FurtherInfoMsgId;
import com.verizon.thingspace.models.GeographicalPath;
import com.verizon.thingspace.models.GeographicalPathDescription;
import com.verizon.thingspace.models.ITISItemContent;
import com.verizon.thingspace.models.ITISItemWrapper;
import com.verizon.thingspace.models.NodeLL;
import com.verizon.thingspace.models.NodeLLmD64b;
import com.verizon.thingspace.models.NodeListLL;
import com.verizon.thingspace.models.NodeOffsetPointLL;
import com.verizon.thingspace.models.Offset;
import com.verizon.thingspace.models.OffsetSystem;
import com.verizon.thingspace.models.containers.AdvisoryItem;
import com.verizon.thingspace.models.containers.DataFrameContent;
import com.verizon.thingspace.models.containers.DataFrameMsgId;
import java.util.Arrays;

DataFrame dataFrame = new DataFrame.Builder(
    FrameTypeEnum.UNKNOWN,
    DataFrameMsgId.fromFurtherInfoMsgId(
        new FurtherInfoMsgId.Builder(
            "1101"
        )
        .build()
    ),
    30,
    200,
    7,
    Arrays.asList(
        new GeographicalPath.Builder()
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
            .build()
    ),
    DataFrameContent.fromAdvisoryContent(
        new AdvisoryContent.Builder(
            Arrays.asList(
                AdvisoryItem.fromITISItemWrapper(
                    new ITISItemWrapper.Builder(
                        new ITISItemContent.Builder(
                            10
                        )
                        .build()
                    )
                    .build()
                )
            )
        )
        .build()
    )
)
.doNotUse1(0)
.startYear(168)
.doNotUse2(0)
.doNotUse3(0)
.doNotUse4(0)
.build();
```

