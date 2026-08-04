
# Place of Use

The customer name and the address of the device's primary place of use. Leave these fields empty to use the account profile address as the primary place of use. These values will be applied to all devices in the request.If the account is enabled for non-geographic MDNs and the device supports it, the primaryPlaceOfUse address will also be used to derive the MDN for the device.

## Structure

`PlaceOfUse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Address` | [`Address`](../../doc/models/address.md) | Required | The customer address for the line's primary place of use, for line usage taxation. | Address getAddress() | setAddress(Address address) |
| `CustomerName` | [`CustomerName`](../../doc/models/customer-name.md) | Required | The customer name to be used for line usage taxation. | CustomerName getCustomerName() | setCustomerName(CustomerName customerName) |

## Example

```java
import com.verizon.thingspace.models.Address;
import com.verizon.thingspace.models.CustomerName;
import com.verizon.thingspace.models.PlaceOfUse;

PlaceOfUse placeOfUse = new PlaceOfUse.Builder(
    new Address.Builder(
        "1600 Pennsylvania Ave NW",
        "Washington",
        "DC",
        "20500",
        "USA"
    )
    .addressLine2("addressLine26")
    .zip4("zip40")
    .phone("phone4")
    .phoneType("phoneType0")
    .emailAddress("emailAddress6")
    .build(),
    new CustomerName.Builder(
        "Zaffod",
        "Beeblebrox"
    )
    .title("President")
    .middleName("middleName8")
    .suffix("suffix0")
    .build()
)
.build();
```

