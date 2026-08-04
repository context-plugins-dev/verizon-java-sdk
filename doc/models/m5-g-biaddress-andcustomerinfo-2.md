
# M5 G Biaddress Andcustomerinfo 2

## Structure

`M5gBiaddressAndcustomerinfo2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `PrimaryPlaceofuse` | [`M5gBiaddressAndcustomerinfo`](../../doc/models/m5-g-biaddress-andcustomerinfo.md) | Optional | - | M5gBiaddressAndcustomerinfo getPrimaryPlaceofuse() | setPrimaryPlaceofuse(M5gBiaddressAndcustomerinfo primaryPlaceofuse) |

## Example

```java
import com.verizon.thingspace.models.M5gBiAddress;
import com.verizon.thingspace.models.M5gBiCustomerName;
import com.verizon.thingspace.models.M5gBiaddressAndcustomerinfo;
import com.verizon.thingspace.models.M5gBiaddressAndcustomerinfo2;
import com.verizon.thingspace.models.M5gBiprimaryPlaceofuse;

M5gBiaddressAndcustomerinfo2 m5gBiaddressAndcustomerinfo2 = new M5gBiaddressAndcustomerinfo2.Builder()
    .primaryPlaceofuse(new M5gBiaddressAndcustomerinfo.Builder()
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
        .build())
    .build();
```

