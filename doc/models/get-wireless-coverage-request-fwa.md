
# Get Wireless Coverage Request FWA

Get wireless coverage FWA.

## Structure

`GetWirelessCoverageRequestFWA`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | Account name.<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `32`, *Pattern*: `^[0-9-]{3,32}$` | String getAccountName() | setAccountName(String accountName) |
| `RequestType` | `String` | Required | Type of request made. FWA for address qualification and NW for Nationwide coverage.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `12`, *Pattern*: `^[A-Za-z]{1,12}$` | String getRequestType() | setRequestType(String requestType) |
| `LocationType` | `String` | Required | Type of location detail.<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `12`, *Pattern*: `^[A-Za-z]{3,12}$` | String getLocationType() | setLocationType(String locationType) |
| `Locations` | [`Locations`](../../doc/models/locations.md) | Required | - | Locations getLocations() | setLocations(Locations locations) |
| `NetworkTypesList` | [`List<NetworkTypeObject>`](../../doc/models/network-type-object.md) | Required | **Constraints**: *Maximum Items*: `100` | List<NetworkTypeObject> getNetworkTypesList() | setNetworkTypesList(List<NetworkTypeObject> networkTypesList) |

## Example

```java
import com.verizon.thingspace.models.AddressItem;
import com.verizon.thingspace.models.GetWirelessCoverageRequestFWA;
import com.verizon.thingspace.models.Locations;
import com.verizon.thingspace.models.NetworkTypeObject;
import java.util.Arrays;

GetWirelessCoverageRequestFWA getWirelessCoverageRequestFWA = new GetWirelessCoverageRequestFWA.Builder(
    "0000123456-00001",
    "NW",
    "ADDRESS",
    new Locations.Builder()
        .addressList(Arrays.asList(
            new AddressItem.Builder()
                .addressLine1("addressLine10")
                .addressLine2("addressLine28")
                .city("city8")
                .state("state4")
                .country("country2")
                .build()
        ))
        .build(),
    Arrays.asList(
        new NetworkTypeObject.Builder()
            .networkType("LTE")
            .build()
    )
)
.build();
```

