
# License Device List

List of all devices.

## Structure

`LicenseDeviceList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceIds` | [`List<LicenseDeviceId>`](../../doc/models/license-device-id.md) | Optional | For 4G devices, IMEI (decimal, up to 15 digits).<br><br>**Constraints**: *Maximum Items*: `100` | List<LicenseDeviceId> getDeviceIds() | setDeviceIds(List<LicenseDeviceId> deviceIds) |
| `Ipaddress` | `String` | Optional | **Constraints**: *Minimum Length*: `3`, *Maximum Length*: `32`, *Pattern*: `^[0-9].[0-9].[0-9].[0-9]{3,32}$` | String getIpaddress() | setIpaddress(String ipaddress) |

## Example

```java
import com.verizon.thingspace.models.LicenseDeviceId;
import com.verizon.thingspace.models.LicenseDeviceList;
import java.util.Arrays;

LicenseDeviceList licenseDeviceList = new LicenseDeviceList.Builder()
    .deviceIds(Arrays.asList(
        new LicenseDeviceId.Builder()
            .id("864508030109877")
            .kind("IMEI")
            .build()
    ))
    .ipaddress("ipAddress8")
    .build();
```

