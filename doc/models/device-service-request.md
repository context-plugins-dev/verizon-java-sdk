
# Device Service Request

Device information.

## Structure

`DeviceServiceRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Imei` | `String` | Required | The International Mobile Equipment Identifier of the device. | String getImei() | setImei(String imei) |
| `BullseyeEnable` | [`HplBullseyeEnable`](../../doc/models/hpl-bullseye-enable.md) | Required | A flag that shows if Hyper Precise is enabled (true) or disabled (false). | HplBullseyeEnable getBullseyeEnable() | setBullseyeEnable(HplBullseyeEnable bullseyeEnable) |

## Example

```java
import com.verizon.thingspace.models.DeviceServiceRequest;
import com.verizon.thingspace.models.HplBullseyeEnable;

DeviceServiceRequest deviceServiceRequest = new DeviceServiceRequest.Builder(
    "15-digit IMEI",
    new HplBullseyeEnable.Builder()
        .bullseyeEnable(true)
        .build()
)
.build();
```

