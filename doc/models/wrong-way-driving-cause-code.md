
# Wrong Way Driving Cause Code

Cause code wrapper for wrong way driving events.

## Structure

`WrongWayDrivingCauseCode`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `WrongWayDriving14` | `int` | Required | The value shall be set to:<br><br>- 0 `unavailable`    - in case further detailed information on wrong way driving event is unavailable,<br>- 1 `wrongLane`      - in case vehicle is driving on a lane for which it has no authorization to use,<br>- 2 `wrongDirection` - in case vehicle is driving in a direction that it is not allowed,<br>- 3-255              - reserved for future usage.<br><br>**Constraints**: `>= 0`, `<= 255` | int getWrongWayDriving14() | setWrongWayDriving14(int wrongWayDriving14) |

## Example

```java
import com.verizon.thingspace.models.WrongWayDrivingCauseCode;

WrongWayDrivingCauseCode wrongWayDrivingCauseCode = new WrongWayDrivingCauseCode.Builder(
    218
)
.build();
```

