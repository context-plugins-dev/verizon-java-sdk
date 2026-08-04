
# Device Profile Request

## Structure

`DeviceProfileRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Devices` | [`List<GIODeviceList>`](../../doc/models/gio-device-list.md) | Optional | **Constraints**: *Maximum Items*: `100` | List<GIODeviceList> getDevices() | setDevices(List<GIODeviceList> devices) |
| `AccountName` | `String` | Optional | **Constraints**: *Minimum Length*: `3`, *Maximum Length*: `32`, *Pattern*: `^[0-9\-]{3,32}$` | String getAccountName() | setAccountName(String accountName) |
| `ServicePlan` | `String` | Optional | **Constraints**: *Minimum Length*: `3`, *Maximum Length*: `32`, *Pattern*: `^[A-Za-z0-9 ]{3,32}$` | String getServicePlan() | setServicePlan(String servicePlan) |

## Example

```java
import com.verizon.thingspace.models.DeviceProfileRequest;
import com.verizon.thingspace.models.GIODeviceId;
import com.verizon.thingspace.models.GIODeviceList;
import java.util.Arrays;

DeviceProfileRequest deviceProfileRequest = new DeviceProfileRequest.Builder()
    .devices(Arrays.asList(
        new GIODeviceList.Builder()
            .deviceIds(Arrays.asList(
                new GIODeviceId.Builder(
                    "kind8",
                    "id0"
                )
                .build()
            ))
            .build(),
        new GIODeviceList.Builder()
            .deviceIds(Arrays.asList(
                new GIODeviceId.Builder(
                    "kind8",
                    "id0"
                )
                .build()
            ))
            .build(),
        new GIODeviceList.Builder()
            .deviceIds(Arrays.asList(
                new GIODeviceId.Builder(
                    "kind8",
                    "id0"
                )
                .build()
            ))
            .build()
    ))
    .accountName("0000123456-00001")
    .servicePlan("service plan name")
    .build();
```

