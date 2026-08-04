
# Get Network Conditions Request

Get network conditions.

## Structure

`GetNetworkConditionsRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | Account name.<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `32`, *Pattern*: `^[0-9-]{3,32}$` | String getAccountName() | setAccountName(String accountName) |
| `LocationType` | `String` | Required | Type of location detail. | String getLocationType() | setLocationType(String locationType) |
| `Coordinates` | [`Coordinates`](../../doc/models/coordinates.md) | Required | Coordinates information. | Coordinates getCoordinates() | setCoordinates(Coordinates coordinates) |

## Example

```java
import com.verizon.thingspace.models.Coordinates;
import com.verizon.thingspace.models.GetNetworkConditionsRequest;

GetNetworkConditionsRequest getNetworkConditionsRequest = new GetNetworkConditionsRequest.Builder(
    "0000123456-00001",
    "LONGLAT",
    new Coordinates.Builder()
        .latitude("-33.84819")
        .longitude("151.22049")
        .build()
)
.build();
```

