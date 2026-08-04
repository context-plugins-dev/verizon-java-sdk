
# Device List IP

## Structure

`DeviceListIP`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceIds` | [`List<PWNDeviceId>`](../../doc/models/pwn-device-id.md) | Required | - | List<PWNDeviceId> getDeviceIds() | setDeviceIds(List<PWNDeviceId> deviceIds) |
| `Ipaddress` | `String` | Required | - | String getIpaddress() | setIpaddress(String ipaddress) |

## Example

```java
import com.verizon.thingspace.models.DeviceListIP;
import com.verizon.thingspace.models.PWNDeviceId;
import java.util.Arrays;

DeviceListIP deviceListIP = new DeviceListIP.Builder(
    Arrays.asList(
        new PWNDeviceId.Builder(
            "99948099913024600000",
            "iccid"
        )
        .build()
    ),
    "10.3.4.5"
)
.build();
```

