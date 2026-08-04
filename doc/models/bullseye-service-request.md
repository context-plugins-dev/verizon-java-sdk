
# Bullseye Service Request

Account number and list of devices.

## Structure

`BullseyeServiceRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceList` | [`List<DeviceServiceRequest>`](../../doc/models/device-service-request.md) | Required | A list of devices. | List<DeviceServiceRequest> getDeviceList() | setDeviceList(List<DeviceServiceRequest> deviceList) |
| `AccountNumber` | `String` | Required | The numeric ID of the account and must include leading zeroes. This value is indentical to `accountName`. | String getAccountNumber() | setAccountNumber(String accountNumber) |

## Example

```java
import com.verizon.thingspace.models.BullseyeServiceRequest;
import com.verizon.thingspace.models.DeviceServiceRequest;
import com.verizon.thingspace.models.HplBullseyeEnable;
import java.util.Arrays;

BullseyeServiceRequest bullseyeServiceRequest = new BullseyeServiceRequest.Builder(
    Arrays.asList(
        new DeviceServiceRequest.Builder(
            "15-digit IMEI",
            new HplBullseyeEnable.Builder()
                .bullseyeEnable(true)
                .build()
        )
        .build()
    ),
    "0000123456-00001"
)
.build();
```

