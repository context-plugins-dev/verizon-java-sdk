
# Bullseye Service Result

Status of Hyper Precise Location on the device.

## Structure

`BullseyeServiceResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountNumber` | `String` | Optional | The numeric ID of the account and must include leading zeroes. This value is indentical to `accountName`. | String getAccountNumber() | setAccountNumber(String accountNumber) |
| `DeviceList` | [`List<DeviceServiceInformation>`](../../doc/models/device-service-information.md) | Optional | List of devices. | List<DeviceServiceInformation> getDeviceList() | setDeviceList(List<DeviceServiceInformation> deviceList) |
| `ResponseType` | [`ApiResponseCode`](../../doc/models/api-response-code.md) | Optional | ResponseCode and/or a message indicating success or failure of the request. | ApiResponseCode getResponseType() | setResponseType(ApiResponseCode responseType) |

## Example

```java
import com.verizon.thingspace.models.ApiResponseCode;
import com.verizon.thingspace.models.BullseyeServiceResult;
import com.verizon.thingspace.models.DeviceServiceInformation;
import com.verizon.thingspace.models.HplBullseyeEnable;
import com.verizon.thingspace.models.ResponseCodeEnum;
import java.util.Arrays;

BullseyeServiceResult bullseyeServiceResult = new BullseyeServiceResult.Builder()
    .accountNumber("0000123456-00001")
    .deviceList(Arrays.asList(
        new DeviceServiceInformation.Builder(
            "imei4",
            new HplBullseyeEnable.Builder()
                .bullseyeEnable(false)
                .build()
        )
        .responseType(new ApiResponseCode.Builder(
                ResponseCodeEnum.INTERNAL_ERROR,
                "message8"
            )
            .build())
        .build()
    ))
    .responseType(new ApiResponseCode.Builder(
        ResponseCodeEnum.INTERNAL_ERROR,
        "message8"
    )
    .build())
    .build();
```

