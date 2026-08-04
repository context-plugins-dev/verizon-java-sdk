
# Sae Info Message

Traveler Information Message (TIM) message and its mandatory fields. The traveler information message is used to send various types of information (advisory and road sign types) to equipped devices.

## Structure

`SaeInfoMessage`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SaeInfo` | [`SaeInfoPayload`](../../doc/models/sae-info-payload.md) | Required | Traveler Information Message (TIM) payload as defined in SAE J2735. | SaeInfoPayload getSaeInfo() | setSaeInfo(SaeInfoPayload saeInfo) |

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
import com.verizon.thingspace.models.SaeInfoMessage;
import com.verizon.thingspace.models.SaeInfoPayload;
import com.verizon.thingspace.models.containers.AdvisoryItem;
import com.verizon.thingspace.models.containers.DataFrameContent;
import com.verizon.thingspace.models.containers.DataFrameMsgId;
import java.util.Arrays;

SaeInfoMessage saeInfoMessage = new SaeInfoMessage.Builder(
    new SaeInfoPayload.Builder(
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
    .build()
)
.build();
```

