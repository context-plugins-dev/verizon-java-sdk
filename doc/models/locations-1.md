
# Locations 1

## Structure

`Locations1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CoordinatesList` | [`List<Coordinates>`](../../doc/models/coordinates.md) | Optional | - | List<Coordinates> getCoordinatesList() | setCoordinatesList(List<Coordinates> coordinatesList) |
| `AddressList` | [`List<AddressItem>`](../../doc/models/address-item.md) | Optional | **Constraints**: *Maximum Items*: `100` | List<AddressItem> getAddressList() | setAddressList(List<AddressItem> addressList) |

## Example

```java
import com.verizon.thingspace.models.AddressItem;
import com.verizon.thingspace.models.Coordinates;
import com.verizon.thingspace.models.Locations1;
import java.util.Arrays;

Locations1 locations1 = new Locations1.Builder()
    .coordinatesList(Arrays.asList(
        new Coordinates.Builder()
            .latitude("latitude6")
            .longitude("longitude4")
            .build(),
        new Coordinates.Builder()
            .latitude("latitude6")
            .longitude("longitude4")
            .build(),
        new Coordinates.Builder()
            .latitude("latitude6")
            .longitude("longitude4")
            .build()
    ))
    .addressList(Arrays.asList(
        new AddressItem.Builder()
            .addressLine1("addressLine10")
            .addressLine2("addressLine28")
            .city("city8")
            .state("state4")
            .country("country2")
            .build()
    ))
    .build();
```

