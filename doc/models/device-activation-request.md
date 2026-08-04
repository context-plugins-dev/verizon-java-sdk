
# Device Activation Request

Request for device status to check availability of activation.

## Structure

`DeviceActivationRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | The name of a billing account. | String getAccountName() | setAccountName(String accountName) |
| `Devices` | [`List<AccountDeviceList>`](../../doc/models/account-device-list.md) | Required | Up to 10,000 devices that you want to move to a different account, specified by device identifier. | List<AccountDeviceList> getDevices() | setDevices(List<AccountDeviceList> devices) |

## Example

```java
import com.verizon.thingspace.models.AccountDeviceList;
import com.verizon.thingspace.models.DeviceActivationRequest;
import com.verizon.thingspace.models.DeviceId;
import java.util.Arrays;

DeviceActivationRequest deviceActivationRequest = new DeviceActivationRequest.Builder(
    "0212345678-00001",
    Arrays.asList(
        new AccountDeviceList.Builder(
            Arrays.asList(
                new DeviceId.Builder(
                    "15-digit IMEI",
                    "imei"
                )
                .build()
            )
        )
        .ipaddress("ipAddress4")
        .build()
    )
)
.build();
```

