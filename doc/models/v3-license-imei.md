
# V3 License IMEI

List of devices.

## Structure

`V3LicenseIMEI`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceList` | `List<String>` | Required | Device IMEI list. | List<String> getDeviceList() | setDeviceList(List<String> deviceList) |

## Example

```java
import com.verizon.thingspace.models.V3LicenseIMEI;
import java.util.Arrays;

V3LicenseIMEI v3LicenseIMEI = new V3LicenseIMEI.Builder(
    Arrays.asList(
        "15-digit IMEI",
        "15-digit IMEI"
    )
)
.build();
```

