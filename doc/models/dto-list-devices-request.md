
# Dto List Devices Request

## Structure

`DtoListDevicesRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountname` | `String` | Optional | The numeric account name, which must include leading zeros | String getAccountname() | setAccountname(String accountname) |
| `Filter` | [`DtoFilter`](../../doc/models/dto-filter.md) | Optional | - | DtoFilter getFilter() | setFilter(DtoFilter filter) |
| `Resourceidentifier` | [`DtoDeviceResourceIdentifier`](../../doc/models/dto-device-resource-identifier.md) | Optional | Device identifiers, one or more are required | DtoDeviceResourceIdentifier getResourceidentifier() | setResourceidentifier(DtoDeviceResourceIdentifier resourceidentifier) |

## Example

```java
import com.verizon.thingspace.models.DtoDeviceResourceIdentifier;
import com.verizon.thingspace.models.DtoFilter;
import com.verizon.thingspace.models.DtoListDevicesRequest;

DtoListDevicesRequest dtoListDevicesRequest = new DtoListDevicesRequest.Builder()
    .accountname("0000123456-00001")
    .filter(new DtoFilter.Builder()
        .expand("$expand0")
        .limitnumber(100)
        .nopagination(false)
        .page("$page0")
        .pagenumber(64)
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

