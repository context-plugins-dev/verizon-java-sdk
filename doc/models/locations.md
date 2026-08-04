
# Locations

Location details.

## Structure

`Locations`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AddressList` | [`List<AddressItem>`](../../doc/models/address-item.md) | Optional | **Constraints**: *Maximum Items*: `100` | List<AddressItem> getAddressList() | setAddressList(List<AddressItem> addressList) |

## Example

```java
import com.verizon.thingspace.models.AddressItem;
import com.verizon.thingspace.models.Locations;
import java.util.Arrays;

Locations locations = new Locations.Builder()
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

