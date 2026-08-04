
# Emergency Vehicle Approaching Cause Code

Cause code wrapper for emergency vehicle approaching events.

## Structure

`EmergencyVehicleApproachingCauseCode`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `EmergencyVehicleApproaching95` | `int` | Required | The value shall be set to:<br><br>- 0 `unavailable`                   - in case further detailed information on the emergency vehicle approaching event is unavailable,<br>- 1 `emergencyVehicleApproaching`   - in case an operating emergency vehicle is approaching,<br>- 2 `prioritizedVehicleApproaching` - in case a prioritized vehicle is approaching,<br>- 3-255                             - reserved for future usage.<br><br>**Constraints**: `>= 0`, `<= 255` | int getEmergencyVehicleApproaching95() | setEmergencyVehicleApproaching95(int emergencyVehicleApproaching95) |

## Example

```java
import com.verizon.thingspace.models.EmergencyVehicleApproachingCauseCode;

EmergencyVehicleApproachingCauseCode emergencyVehicleApproachingCauseCode = new EmergencyVehicleApproachingCauseCode.Builder(
    220
)
.build();
```

