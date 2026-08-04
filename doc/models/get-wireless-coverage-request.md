
# Get Wireless Coverage Request

Get wireless coverage.

## Structure

`GetWirelessCoverageRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | Account name.<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `32`, *Pattern*: `^[0-9-]{3,32}$` | String getAccountName() | setAccountName(String accountName) |
| `RequestType` | `String` | Required | Type of request made. FWA for address qualification and NW for Nationwide coverage.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `12`, *Pattern*: `^[A-Za-z]{1,12}$` | String getRequestType() | setRequestType(String requestType) |
| `LocationType` | `String` | Required | Type of location detail. | String getLocationType() | setLocationType(String locationType) |
| `Locations` | [`Locationscoord`](../../doc/models/locationscoord.md) | Required | - | Locationscoord getLocations() | setLocations(Locationscoord locations) |
| `NetworkTypesList` | [`List<NetworkTypeObject>`](../../doc/models/network-type-object.md) | Required | **Constraints**: *Maximum Items*: `100` | List<NetworkTypeObject> getNetworkTypesList() | setNetworkTypesList(List<NetworkTypeObject> networkTypesList) |

## Example

```java
import com.verizon.thingspace.models.Coordinates;
import com.verizon.thingspace.models.GetWirelessCoverageRequest;
import com.verizon.thingspace.models.Locationscoord;
import com.verizon.thingspace.models.NetworkTypeObject;
import java.util.Arrays;

GetWirelessCoverageRequest getWirelessCoverageRequest = new GetWirelessCoverageRequest.Builder(
    "0000123456-00001",
    "NW",
    "LONGLAT",
    new Locationscoord.Builder()
        .coordinatesList(Arrays.asList(
            new Coordinates.Builder()
                .latitude("latitude6")
                .longitude("longitude4")
                .build(),
            new Coordinates.Builder()
                .latitude("latitude6")
                .longitude("longitude4")
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

