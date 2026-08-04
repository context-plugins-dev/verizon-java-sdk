
# V2 License IMEI

IMEIs of the devices to assign or remove licenses.

## Structure

`V2LicenseIMEI`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Optional | Account name. | String getAccountName() | setAccountName(String accountName) |
| `DeviceList` | `List<String>` | Required | Device IMEI list. | List<String> getDeviceList() | setDeviceList(List<String> deviceList) |

## Example

```java
import com.verizon.thingspace.models.V2LicenseIMEI;
import java.util.Arrays;

V2LicenseIMEI v2LicenseIMEI = new V2LicenseIMEI.Builder(
    Arrays.asList(
        "990003425730524",
        "990000473475967"
    )
)
.accountName("accountName4")
.build();
```

