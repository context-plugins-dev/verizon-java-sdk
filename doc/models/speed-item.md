
# Speed Item

Defines the acceptable speed range for road users in m/s. Messages are triggered when:
1. The road user's speed is below the required minimum OR
2. The road user's speed is above the acceptable maximum AND
3. The associated TriggerConditions are met.

Example: For the speed range of 10-20 m/s and a TriggerCondition of 'user inside geofence', the message is sent if the user's speed is below 10 m/s or above 20 m/s while in the geofence area.

## Structure

`SpeedItem`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Speed` | [`SpeedRange`](../../doc/models/speed-range.md) | Required | Acceptable speed range for road users in m/s. | SpeedRange getSpeed() | setSpeed(SpeedRange speed) |

## Example

```java
import com.verizon.thingspace.models.SpeedItem;
import com.verizon.thingspace.models.SpeedRange;

SpeedItem speedItem = new SpeedItem.Builder(
    new SpeedRange.Builder(
        64.76D,
        138.18D
    )
    .build()
)
.build();
```

