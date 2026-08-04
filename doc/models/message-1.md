
# Message 1

## Structure

`Message1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `IsPrivate` | `boolean` | Required | Defines whether the message is private or public.<br>Private messages are published under the Vendor ID defined in the configuration and only visible to devices of selected vendors.<br>Public messages are published under the Public vendor and are visible to all the users. | boolean getIsPrivate() | setIsPrivate(boolean isPrivate) |
| `RoadUserType` | [`List<RoadUserTypesEnum>`](../../doc/models/road-user-types-enum.md) | Required | Type of the Road User.<br><br>**Constraints**: *Minimum Items*: `1`, *Maximum Items*: `2` | List<RoadUserTypesEnum> getRoadUserType() | setRoadUserType(List<RoadUserTypesEnum> roadUserType) |
| `TriggerConditions` | [`List<TriggerConditionEnum>`](../../doc/models/trigger-condition-enum.md) | Required | Trigger conditions that define on which road user action the message will be sent. If multiple Trigger Conditions are defined any of them will trigger the message.<br><br>**Constraints**: *Minimum Items*: `1`, *Maximum Items*: `3` | List<TriggerConditionEnum> getTriggerConditions() | setTriggerConditions(List<TriggerConditionEnum> triggerConditions) |
| `Limits` | [`List<Limits>`](../../doc/models/containers/limits.md) | Optional | List of limitations. These limitations can be used for making the trigger condition more precise by defining speed and motion direction requirements to be met before the messages are sent out.<br><br>**Constraints**: *Minimum Items*: `1`, *Maximum Items*: `2` | List<Limits> getLimits() | setLimits(List<Limits> limits) |
| `DistributionType` | [`List<DistributionTypesEnum>`](../../doc/models/distribution-types-enum.md) | Optional | Type of the distribution.<br><br>**Constraints**: *Minimum Items*: `1`, *Maximum Items*: `2` | List<DistributionTypesEnum> getDistributionType() | setDistributionType(List<DistributionTypesEnum> distributionType) |
| `DistributionSchedule` | [`DistributionSchedule`](../../doc/models/distribution-schedule.md) | Optional | The distribution schedule parameters for broadcast messages. | DistributionSchedule getDistributionSchedule() | setDistributionSchedule(DistributionSchedule distributionSchedule) |
| `SaeAlert` | [`SaeAlertPayload`](../../doc/models/sae-alert-payload.md) | Required | Road Side Alert (RSA) message payload as defined in SAE J2735. | SaeAlertPayload getSaeAlert() | setSaeAlert(SaeAlertPayload saeAlert) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.DistributionSchedule;
import com.verizon.thingspace.models.DistributionTypesEnum;
import com.verizon.thingspace.models.Message1;
import com.verizon.thingspace.models.RoadUserTypesEnum;
import com.verizon.thingspace.models.SaeAlertPayload;
import com.verizon.thingspace.models.SpeedItem;
import com.verizon.thingspace.models.SpeedRange;
import com.verizon.thingspace.models.TriggerConditionEnum;
import com.verizon.thingspace.models.containers.Limits;
import java.util.Arrays;

Message1 message1 = new Message1.Builder(
    false,
    Arrays.asList(
        RoadUserTypesEnum.VULNERABLEROADUSER
    ),
    Arrays.asList(
        TriggerConditionEnum.CROSSING
    ),
    new SaeAlertPayload.Builder(
        160
    )
    .msgCnt(0)
    .description(Arrays.asList(
            15,
            16
        ))
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

