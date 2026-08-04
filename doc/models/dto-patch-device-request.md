
# Dto Patch Device Request

## Structure

`DtoPatchDeviceRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountname` | `String` | Optional | The numeric account name, which must include leading zeros | String getAccountname() | setAccountname(String accountname) |
| `Device` | [`ResourceDevice`](../../doc/models/resource-device.md) | Optional | - | ResourceDevice getDevice() | setDevice(ResourceDevice device) |
| `Resourceidentifier` | [`DtoDeviceResourceIdentifier`](../../doc/models/dto-device-resource-identifier.md) | Optional | Device identifiers, one or more are required | DtoDeviceResourceIdentifier getResourceidentifier() | setResourceidentifier(DtoDeviceResourceIdentifier resourceidentifier) |

## Example

```java
import com.verizon.thingspace.ApiHelper;
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.DtoDeviceResourceIdentifier;
import com.verizon.thingspace.models.DtoPatchDeviceRequest;
import com.verizon.thingspace.models.ResourceDevice;
import java.io.IOException;
import java.util.LinkedHashMap;

DtoPatchDeviceRequest dtoPatchDeviceRequest = new DtoPatchDeviceRequest.Builder()
    .accountname("0000123456-00001")
    .device(new ResourceDevice.Builder(
        DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"),
        "foreignid4",
        DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"),
        "state2",
        "versionid8"
    )
    .accountclientid("accountclientid2")
    .billingaccountid("billingaccountid2")
    .chipset("chipset6")
    .customdata(new LinkedHashMap<String, Object>() {{
            put("key0", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"));
        }})
    .description("description6")
    .build())
    .resourceidentifier(new DtoDeviceResourceIdentifier.Builder()
        .deveui("deveui2")
        .deviceid("deviceid6")
        .esn(86)
        .iccid("iccid0")
        .imei(2)
        .build())
    .build();
```

