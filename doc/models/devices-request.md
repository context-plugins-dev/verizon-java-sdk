
# Devices Request

Request body for retrieving devices based on vendorID and optional filters

## Structure

`DevicesRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `VendorId` | `String` | Required | The ID the vendor wants its devices to be registered under. E.g. Verizon, GM, Ford, etc.<br><br>**Constraints**: *Maximum Length*: `64`, *Pattern*: `^[a-zA-Z0-9]+$` | String getVendorId() | setVendorId(String vendorId) |
| `Filter` | [`DevicesRequestFilter`](../../doc/models/containers/devices-request-filter.md) | Optional | This is a container for one-of cases. | DevicesRequestFilter getFilter() | setFilter(DevicesRequestFilter filter) |

## Example

```java
import com.verizon.thingspace.models.ClientSubtypeEnum;
import com.verizon.thingspace.models.DevicesFilter;
import com.verizon.thingspace.models.DevicesRequest;
import com.verizon.thingspace.models.EtxClientTypeEnum;
import com.verizon.thingspace.models.containers.DevicesRequestFilter;

DevicesRequest devicesRequest = new DevicesRequest.Builder(
    "VerizonETX"
)
.filter(DevicesRequestFilter.fromDevicesFilter(
        new DevicesFilter.Builder()
            .clientType(EtxClientTypeEnum.TRAFFICLIGHTCONTROLLER)
            .clientSubtype(ClientSubtypeEnum.EMERGENCYVEHICLE)
            .mecId("MecId4")
            .pageSize(182)
            .build()
    ))
.build();
```

