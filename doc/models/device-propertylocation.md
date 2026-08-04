
# Device Propertylocation

## Structure

`DevicePropertylocation`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Latitude` | `String` | Optional | - | String getLatitude() | setLatitude(String latitude) |
| `Longitude` | `String` | Optional | - | String getLongitude() | setLongitude(String longitude) |

## Example

```java
import com.verizon.thingspace.models.DevicePropertylocation;

DevicePropertylocation devicePropertylocation = new DevicePropertylocation.Builder()
    .latitude("37.2314796")
    .longitude("-119.4692153")
    .build();
```

