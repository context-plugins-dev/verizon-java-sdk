
# Activate Device Profile Request

## Structure

`ActivateDeviceProfileRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Devices` | [`List<DeviceList>`](../../doc/models/device-list.md) | Required | **Constraints**: *Maximum Items*: `100` | List<DeviceList> getDevices() | setDevices(List<DeviceList> devices) |
| `AccountName` | `String` | Required | - | String getAccountName() | setAccountName(String accountName) |
| `ServicePlan` | `String` | Optional | - | String getServicePlan() | setServicePlan(String servicePlan) |
| `MdnZipCode` | `String` | Optional | - | String getMdnZipCode() | setMdnZipCode(String mdnZipCode) |

## Example

```java
import com.verizon.thingspace.models.ActivateDeviceProfileRequest;
import com.verizon.thingspace.models.DeviceId;
import com.verizon.thingspace.models.DeviceList;
import java.util.Arrays;

ActivateDeviceProfileRequest activateDeviceProfileRequest = new ActivateDeviceProfileRequest.Builder(
    Arrays.asList(
        new DeviceList.Builder()
            .deviceIds(Arrays.asList(
                new DeviceId.Builder(
                    "id0",
                    "kind8"
                )
                .build()
            ))
            .build()
    ),
    "0000123456-00001"
)
.servicePlan("The service plan name")
.mdnZipCode("five digit zip code")
.build();
```

