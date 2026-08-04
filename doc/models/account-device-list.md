
# Account Device List

A list of deviceId objects to use when requesting information from multiple devices.

## Structure

`AccountDeviceList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceIds` | [`List<DeviceId>`](../../doc/models/device-id.md) | Required | All identifiers for the device. | List<DeviceId> getDeviceIds() | setDeviceIds(List<DeviceId> deviceIds) |
| `Ipaddress` | `String` | Optional | **Constraints**: *Minimum Length*: `3`, *Maximum Length*: `32`, *Pattern*: `^[0-9].[0-9].[0-9].[0-9]{3,32}$` | String getIpaddress() | setIpaddress(String ipaddress) |

## Example

```java
import com.verizon.thingspace.models.AccountDeviceList;
import com.verizon.thingspace.models.DeviceId;
import java.util.Arrays;

AccountDeviceList accountDeviceList = new AccountDeviceList.Builder(
    Arrays.asList(
        new DeviceId.Builder(
            "990013907835573",
            "imei"
        )
        .build(),
        new DeviceId.Builder(
            "89141390780800784259",
            "iccid"
        )
        .build()
    )
)
.ipaddress("ipAddress0")
.build();
```

