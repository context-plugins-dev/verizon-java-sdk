
# Sae Info Payload

Traveler Information Message (TIM) payload as defined in SAE J2735.

## Structure

`SaeInfoPayload`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `MsgCnt` | `Integer` | Optional | It is used to provide a sequence number within a stream of messages with the same DSRCmsgID (here RoadSideAlert) and from the same sender.<br><br>**Default**: `0`<br><br>**Constraints**: `>= 0`, `<= 127` | Integer getMsgCnt() | setMsgCnt(Integer msgCnt) |
| `TimeStamp` | `Integer` | Optional | The number of elapsed minutes of the current year in the time system being used (typically UTC time).<br>-- the value 527040 shall be used for invalid<br><br>**Constraints**: `>= 0`, `<= 527040` | Integer getTimeStamp() | setTimeStamp(Integer timeStamp) |
| `PacketID` | `String` | Optional | Provides a relatively unique value which can be used to connect to (link to) other supporting messages in other formats.<br><br>The value is described as a 18-character hexadecimal string.<br><br>**Constraints**: *Pattern*: `^[0-9A-Fa-f]{18}$` | String getPacketID() | setPacketID(String packetID) |
| `UrlB` | `String` | Optional | A valid internet style URI/URL in the form of a text string which will form the base of a compound string which, when<br>combined with the URL-short data element, will link to the designated resource.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `45` | String getUrlB() | setUrlB(String urlB) |
| `DataFrames` | [`List<DataFrame>`](../../doc/models/data-frame.md) | Required | List of data frames.<br><br>**Constraints**: *Minimum Items*: `1`, *Maximum Items*: `8` | List<DataFrame> getDataFrames() | setDataFrames(List<DataFrame> dataFrames) |

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
import com.verizon.thingspace.models.SaeInfoPayload;
import com.verizon.thingspace.models.containers.AdvisoryItem;
import com.verizon.thingspace.models.containers.DataFrameContent;
import com.verizon.thingspace.models.containers.DataFrameMsgId;
import java.util.Arrays;

SaeInfoPayload saeInfoPayload = new SaeInfoPayload.Builder(
    Arrays.asList(
        new DataFrame.Builder(
            FrameTypeEnum.UNKNOWN,
            DataFrameMsgId.fromFurtherInfoMsgId(
                new FurtherInfoMsgId.Builder(
                    "1101"
                )
                .build()
            ),
            186,
            44,
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
        .startYear(12)
        .doNotUse2(0)
        .doNotUse3(0)
        .doNotUse4(0)
        .build()
    )
)
.msgCnt(0)
.timeStamp(5)
.packetID("B343B343B343B343A5")
.urlB("http://example.com")
.build();
```

