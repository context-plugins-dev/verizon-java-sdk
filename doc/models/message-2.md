
# Message 2

## Structure

`Message2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `IsPrivate` | `boolean` | Required | Defines whether the message is private or public.<br>Private messages are published under the Vendor ID defined in the configuration and only visible to devices of selected vendors.<br>Public messages are published under the Public vendor and are visible to all the users. | boolean getIsPrivate() | setIsPrivate(boolean isPrivate) |
| `RoadUserType` | [`List<RoadUserTypesEnum>`](../../doc/models/road-user-types-enum.md) | Required | Type of the Road User.<br><br>**Constraints**: *Minimum Items*: `1`, *Maximum Items*: `2` | List<RoadUserTypesEnum> getRoadUserType() | setRoadUserType(List<RoadUserTypesEnum> roadUserType) |
| `TriggerConditions` | [`List<TriggerConditionEnum>`](../../doc/models/trigger-condition-enum.md) | Required | Trigger conditions that define on which road user action the message will be sent. If multiple Trigger Conditions are defined any of them will trigger the message.<br><br>**Constraints**: *Minimum Items*: `1`, *Maximum Items*: `3` | List<TriggerConditionEnum> getTriggerConditions() | setTriggerConditions(List<TriggerConditionEnum> triggerConditions) |
| `Limits` | [`List<Limits>`](../../doc/models/containers/limits.md) | Optional | List of limitations. These limitations can be used for making the trigger condition more precise by defining speed and motion direction requirements to be met before the messages are sent out.<br><br>**Constraints**: *Minimum Items*: `1`, *Maximum Items*: `2` | List<Limits> getLimits() | setLimits(List<Limits> limits) |
| `DistributionType` | [`List<DistributionTypesEnum>`](../../doc/models/distribution-types-enum.md) | Optional | Type of the distribution.<br><br>**Constraints**: *Minimum Items*: `1`, *Maximum Items*: `2` | List<DistributionTypesEnum> getDistributionType() | setDistributionType(List<DistributionTypesEnum> distributionType) |
| `DistributionSchedule` | [`DistributionSchedule`](../../doc/models/distribution-schedule.md) | Optional | The distribution schedule parameters for broadcast messages. | DistributionSchedule getDistributionSchedule() | setDistributionSchedule(DistributionSchedule distributionSchedule) |
| `SaeInfo` | [`SaeInfoPayload`](../../doc/models/sae-info-payload.md) | Required | Traveler Information Message (TIM) payload as defined in SAE J2735. | SaeInfoPayload getSaeInfo() | setSaeInfo(SaeInfoPayload saeInfo) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.AdvisoryContent;
import com.verizon.thingspace.models.DataFrame;
import com.verizon.thingspace.models.DistributionSchedule;
import com.verizon.thingspace.models.DistributionTypesEnum;
import com.verizon.thingspace.models.FrameTypeEnum;
import com.verizon.thingspace.models.FurtherInfoMsgId;
import com.verizon.thingspace.models.GeographicalPath;
import com.verizon.thingspace.models.GeographicalPathDescription;
import com.verizon.thingspace.models.ITISItemContent;
import com.verizon.thingspace.models.ITISItemWrapper;
import com.verizon.thingspace.models.Message2;
import com.verizon.thingspace.models.NodeLL;
import com.verizon.thingspace.models.NodeLLmD64b;
import com.verizon.thingspace.models.NodeListLL;
import com.verizon.thingspace.models.NodeOffsetPointLL;
import com.verizon.thingspace.models.Offset;
import com.verizon.thingspace.models.OffsetSystem;
import com.verizon.thingspace.models.RoadUserTypesEnum;
import com.verizon.thingspace.models.SaeInfoPayload;
import com.verizon.thingspace.models.SpeedItem;
import com.verizon.thingspace.models.SpeedRange;
import com.verizon.thingspace.models.TriggerConditionEnum;
import com.verizon.thingspace.models.containers.AdvisoryItem;
import com.verizon.thingspace.models.containers.DataFrameContent;
import com.verizon.thingspace.models.containers.DataFrameMsgId;
import com.verizon.thingspace.models.containers.Limits;
import java.util.Arrays;

Message2 message2 = new Message2.Builder(
    false,
    Arrays.asList(
        RoadUserTypesEnum.VULNERABLEROADUSER,
        RoadUserTypesEnum.VEHICLE
    ),
    Arrays.asList(
        TriggerConditionEnum.CROSSING,
        TriggerConditionEnum.ENTER,
        TriggerConditionEnum.LEAVE
    ),
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
.limits(Arrays.asList(
        Limits.fromSpeedItem(
            new SpeedItem.Builder(
                new SpeedRange.Builder(
                    64.76D,
                    138.18D
                )
                .build()
            )
            .build()
        ),
        Limits.fromSpeedItem(
            new SpeedItem.Builder(
                new SpeedRange.Builder(
                    64.76D,
                    138.18D
                )
                .build()
            )
            .build()
        ),
        Limits.fromSpeedItem(
            new SpeedItem.Builder(
                new SpeedRange.Builder(
                    64.76D,
                    138.18D
                )
                .build()
            )
            .build()
        )
    ))
.distributionType(Arrays.asList(
        DistributionTypesEnum.BROADCAST,
        DistributionTypesEnum.TARGETED,
        DistributionTypesEnum.BROADCAST
    ))
.distributionSchedule(new DistributionSchedule.Builder(
        90,
        88
    )
    .startTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .build())
.build();
```

