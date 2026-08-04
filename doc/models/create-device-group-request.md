
# Create Device Group Request

Create request for a new device group and optionally add devices to the group.

## Structure

`CreateDeviceGroupRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | The Verizon billing account that the device group will belong to. An account name is usually numeric, and must include any leading zeros. | String getAccountName() | setAccountName(String accountName) |
| `GroupDescription` | `String` | Required | A description for the device group. | String getGroupDescription() | setGroupDescription(String groupDescription) |
| `GroupName` | `String` | Required | The name for the new device group. This name must be unique within the specified account. | String getGroupName() | setGroupName(String groupName) |
| `DevicesToAdd` | [`List<DeviceId>`](../../doc/models/device-id.md) | Optional | Zero or more devices to add to the device group. You can use POST /devices/actions/list to get a list of all devices in the account. | List<DeviceId> getDevicesToAdd() | setDevicesToAdd(List<DeviceId> devicesToAdd) |

## Example

```java
import com.verizon.thingspace.models.CreateDeviceGroupRequest;
import com.verizon.thingspace.models.DeviceId;
import java.util.Arrays;

CreateDeviceGroupRequest createDeviceGroupRequest = new CreateDeviceGroupRequest.Builder(
    "10001234-0001",
    "Nevada tank level monitors.",
    "NV tanks"
)
.devicesToAdd(Arrays.asList(
        new DeviceId.Builder(
            "990003420535537",
            "imei"
        )
        .build()
    ))
.build();
```

