
# Dto Last Reported Time Request

## Structure

`DtoLastReportedTimeRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountname` | `String` | Optional | The numeric account name, which must include leading zeros | String getAccountname() | setAccountname(String accountname) |
| `Resourceidentifier` | [`DtoDeviceResourceIdentifier`](../../doc/models/dto-device-resource-identifier.md) | Optional | Device identifiers, one or more are required | DtoDeviceResourceIdentifier getResourceidentifier() | setResourceidentifier(DtoDeviceResourceIdentifier resourceidentifier) |

## Example

```java
import com.verizon.thingspace.models.DtoDeviceResourceIdentifier;
import com.verizon.thingspace.models.DtoLastReportedTimeRequest;

DtoLastReportedTimeRequest dtoLastReportedTimeRequest = new DtoLastReportedTimeRequest.Builder()
    .accountname("0000123456-00001")
    .resourceidentifier(new DtoDeviceResourceIdentifier.Builder()
        .deveui("deveui2")
        .deviceid("deviceid6")
        .esn(86)
        .iccid("iccid0")
        .imei(2)
        .build())
    .build();
```

