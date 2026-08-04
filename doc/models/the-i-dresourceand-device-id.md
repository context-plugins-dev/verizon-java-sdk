
# The I Dresourceand Device ID

## Structure

`TheIDresourceandDeviceID`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Optional | UUID of the user record, assigned at creation | String getId() | setId(String id) |
| `Deviceid` | `String` | Optional | This is a UUID value of the device created when the device is onboarded | String getDeviceid() | setDeviceid(String deviceid) |

## Example

```java
import com.verizon.thingspace.models.TheIDresourceandDeviceID;

TheIDresourceandDeviceID theIDresourceandDeviceID = new TheIDresourceandDeviceID.Builder()
    .id("id6")
    .deviceid("The UUID of the device")
    .build();
```

