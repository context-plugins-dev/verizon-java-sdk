
# Device Service Information

Device service information.

## Structure

`DeviceServiceInformation`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ResponseType` | [`ApiResponseCode`](../../doc/models/api-response-code.md) | Optional | ResponseCode and/or a message indicating success or failure of the request. | ApiResponseCode getResponseType() | setResponseType(ApiResponseCode responseType) |
| `Imei` | `String` | Required | The International Mobile Equipment Identifier of the device. | String getImei() | setImei(String imei) |
| `BullseyeEnable` | [`HplBullseyeEnable`](../../doc/models/hpl-bullseye-enable.md) | Required | A flag that shows if Hyper Precise is enabled (true) or disabled (false). | HplBullseyeEnable getBullseyeEnable() | setBullseyeEnable(HplBullseyeEnable bullseyeEnable) |

## Example

```java
import com.verizon.thingspace.models.ApiResponseCode;
import com.verizon.thingspace.models.DeviceServiceInformation;
import com.verizon.thingspace.models.HplBullseyeEnable;
import com.verizon.thingspace.models.ResponseCodeEnum;

DeviceServiceInformation deviceServiceInformation = new DeviceServiceInformation.Builder(
    "15-digit IMEI",
    new HplBullseyeEnable.Builder()
        .bullseyeEnable(true)
        .build()
)
.responseType(new ApiResponseCode.Builder(
        ResponseCodeEnum.INTERNAL_ERROR,
        "message8"
    )
    .build())
.build();
```

