
# M5 G Biprimary Placeofuse

## Structure

`M5gBiprimaryPlaceofuse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Address` | [`M5gBiAddress`](../../doc/models/m5-g-bi-address.md) | Optional | - | M5gBiAddress getAddress() | setAddress(M5gBiAddress address) |
| `CustomerName` | [`M5gBiCustomerName`](../../doc/models/m5-g-bi-customer-name.md) | Optional | - | M5gBiCustomerName getCustomerName() | setCustomerName(M5gBiCustomerName customerName) |

## Example

```java
import com.verizon.thingspace.models.M5gBiAddress;
import com.verizon.thingspace.models.M5gBiCustomerName;
import com.verizon.thingspace.models.M5gBiprimaryPlaceofuse;

M5gBiprimaryPlaceofuse m5gBiprimaryPlaceofuse = new M5gBiprimaryPlaceofuse.Builder()
    .address(new M5gBiAddress.Builder()
        .addressLine1("addressLine18")
        .city("city6")
        .state("state2")
        .zip("zip0")
        .zip4("zip+48")
        .build())
    .customerName(new M5gBiCustomerName.Builder()
        .firstName("firstName4")
        .lastName("lastName4")
        .middleName("middleName8")
        .title("title4")
        .suffex("suffex4")
        .build())
    .build();
```

