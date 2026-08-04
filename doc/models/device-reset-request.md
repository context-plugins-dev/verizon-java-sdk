
# Device Reset Request

Request body to Performs a device reboot.

## Structure

`DeviceResetRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Optional | The name of the account. An account name is usually numeric, and must include any leading zeros. | String getAccountName() | setAccountName(String accountName) |
| `Action` | `String` | Optional | The action you want to take on the device. | String getAction() | setAction(String action) |
| `Devices` | [`List<Device>`](../../doc/models/device.md) | Optional | The devices for which you want to perform a factory reset or reboot. | List<Device> getDevices() | setDevices(List<Device> devices) |

## Example

```java
import com.verizon.thingspace.models.Device;
import com.verizon.thingspace.models.DeviceResetRequest;
import java.util.Arrays;

DeviceResetRequest deviceResetRequest = new DeviceResetRequest.Builder()
    .accountName("0642233522-00003")
    .action("reboot")
    .devices(Arrays.asList(
        new Device.Builder(
            "id4",
            "kind2"
        )
        .build()
    ))
    .build();
```

