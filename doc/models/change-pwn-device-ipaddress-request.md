
# Change PWN Device Ipaddress Request

## Structure

`ChangePWNDeviceIpaddressRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | - | String getAccountName() | setAccountName(String accountName) |
| `DeviceList` | [`List<DeviceListIP>`](../../doc/models/device-list-ip.md) | Required | - | List<DeviceListIP> getDeviceList() | setDeviceList(List<DeviceListIP> deviceList) |

## Example

```java
import com.verizon.thingspace.models.ChangePWNDeviceIpaddressRequest;
import com.verizon.thingspace.models.DeviceListIP;
import com.verizon.thingspace.models.PWNDeviceId;
import java.util.Arrays;

ChangePWNDeviceIpaddressRequest changePWNDeviceIpaddressRequest = new ChangePWNDeviceIpaddressRequest.Builder(
    "0342351414-00001",
    Arrays.asList(
        new DeviceListIP.Builder(
            Arrays.asList(
                new PWNDeviceId.Builder(
                    "99948099913024600000",
                    "iccid"
                )
                .build()
            ),
            "10.3.4.5"
        )
        .build(),
        new DeviceListIP.Builder(
            Arrays.asList(
                new PWNDeviceId.Builder(
                    "999480500019111000001",
                    "iccid"
                )
                .build()
            ),
            "10.4.5.7"
        )
        .build()
    )
)
.build();
```

