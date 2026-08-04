
# M5 G Biaddress Andcustomerinfo

## Structure

`M5gBiaddressAndcustomerinfo`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `PrimaryPlaceofuse` | [`M5gBiprimaryPlaceofuse`](../../doc/models/m5-g-biprimary-placeofuse.md) | Optional | - | M5gBiprimaryPlaceofuse getPrimaryPlaceofuse() | setPrimaryPlaceofuse(M5gBiprimaryPlaceofuse primaryPlaceofuse) |

## Example

```java
import com.verizon.thingspace.models.M5gBiAddress;
import com.verizon.thingspace.models.M5gBiCustomerName;
import com.verizon.thingspace.models.M5gBiaddressAndcustomerinfo;
import com.verizon.thingspace.models.M5gBiprimaryPlaceofuse;

M5gBiaddressAndcustomerinfo m5gBiaddressAndcustomerinfo = new M5gBiaddressAndcustomerinfo.Builder()
    .primaryPlaceofuse(new M5gBiprimaryPlaceofuse.Builder()
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
        .build())
    .build();
```

