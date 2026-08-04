
# Device IMEI

Device IMEI list.

## Structure

`DeviceIMEI`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceList` | `List<String>` | Required | Device IMEI list. | List<String> getDeviceList() | setDeviceList(List<String> deviceList) |

## Example

```java
import com.verizon.thingspace.models.DeviceIMEI;
import java.util.Arrays;

DeviceIMEI deviceIMEI = new DeviceIMEI.Builder(
    Arrays.asList(
        "15-digit IMEI"
    )
)
.build();
```

