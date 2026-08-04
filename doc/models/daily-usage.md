
# Daily Usage

## Structure

`DailyUsage`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceId` | [`GIODeviceId`](../../doc/models/gio-device-id.md) | Optional | - | GIODeviceId getDeviceId() | setDeviceId(GIODeviceId deviceId) |
| `Earliest` | `String` | Optional | The start date of the time period queried as "$datetime"<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `32`, *Pattern*: `^[A-Za-z0-9]{3,32}$` | String getEarliest() | setEarliest(String earliest) |
| `Latest` | `String` | Optional | The end date of the time period being queried as "$datetime"<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `32`, *Pattern*: `^[A-Za-z0-9]{3,32}$` | String getLatest() | setLatest(String latest) |

## Example

```java
import com.verizon.thingspace.models.DailyUsage;
import com.verizon.thingspace.models.GIODeviceId;

DailyUsage dailyUsage = new DailyUsage.Builder()
    .deviceId(new GIODeviceId.Builder(
        "kind8",
        "id0"
    )
    .build())
    .earliest("earliest2")
    .latest("latest8")
    .build();
```

