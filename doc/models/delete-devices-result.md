
# Delete Devices Result

Response for a request made to delete a device.

## Structure

`DeleteDevicesResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceIds` | [`DeleteDevicesResultDeviceIds`](../../doc/models/containers/delete-devices-result-device-ids.md) | Optional | This is a container for one-of cases. | DeleteDevicesResultDeviceIds getDeviceIds() | setDeviceIds(DeleteDevicesResultDeviceIds deviceIds) |
| `Status` | `String` | Optional | “Success” if the device was deleted, or “Failed” if there was a problem. | String getStatus() | setStatus(String status) |
| `Message` | `String` | Optional | Not present if status=Success. One of these messages if status=Failed:The device is not in deactivate state.The user does not have access to delete the device. | String getMessage() | setMessage(String message) |

## Example

```java
import com.verizon.thingspace.models.DeleteDevicesResult;
import com.verizon.thingspace.models.DeviceId;
import com.verizon.thingspace.models.containers.DeleteDevicesResultDeviceIds;
import java.util.Arrays;

DeleteDevicesResult deleteDevicesResult = new DeleteDevicesResult.Builder()
    .deviceIds(DeleteDevicesResultDeviceIds.fromListOfDeviceId(
        Arrays.asList(
            new DeviceId.Builder(
                "09005470263",
                "esn"
            )
            .build()
        )
    ))
    .status("Success")
    .message("message8")
    .build();
```

