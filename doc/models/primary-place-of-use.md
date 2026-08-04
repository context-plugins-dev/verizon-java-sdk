
# Primary Place of Use

## Structure

`PrimaryPlaceOfUse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CustomerName` | [`List<CustomerName>`](../../doc/models/customer-name.md) | Optional | **Constraints**: *Maximum Items*: `5` | List<CustomerName> getCustomerName() | setCustomerName(List<CustomerName> customerName) |
| `Address` | [`List<Address>`](../../doc/models/address.md) | Optional | **Constraints**: *Maximum Items*: `5` | List<Address> getAddress() | setAddress(List<Address> address) |

## Example

```java
import com.verizon.thingspace.models.Address;
import com.verizon.thingspace.models.CustomerName;
import com.verizon.thingspace.models.PrimaryPlaceOfUse;
import java.util.Arrays;

PrimaryPlaceOfUse primaryPlaceOfUse = new PrimaryPlaceOfUse.Builder()
    .customerName(Arrays.asList(
        new CustomerName.Builder(
            "firstName4",
            "lastName4"
        )
        .title("title4")
        .middleName("middleName8")
        .suffix("suffix0")
        .build()
    ))
    .address(Arrays.asList(
        new Address.Builder(
            "addressLine18",
            "city6",
            "state2",
            "zip0",
            "country0"
        )
        .addressLine2("addressLine26")
        .zip4("zip40")
        .phone("phone4")
        .phoneType("phoneType0")
        .emailAddress("emailAddress6")
        .build(),
        new Address.Builder(
            "addressLine18",
            "city6",
            "state2",
            "zip0",
            "country0"
        )
        .addressLine2("addressLine26")
        .zip4("zip40")
        .phone("phone4")
        .phoneType("phoneType0")
        .emailAddress("emailAddress6")
        .build()
    ))
    .build();
```

