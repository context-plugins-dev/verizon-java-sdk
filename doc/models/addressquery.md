
# Addressquery

## Structure

`Addressquery`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Address` | [`List<Address>`](../../doc/models/address.md) | Optional | **Constraints**: *Maximum Items*: `5` | List<Address> getAddress() | setAddress(List<Address> address) |

## Example

```java
import com.verizon.thingspace.models.Address;
import com.verizon.thingspace.models.Addressquery;
import java.util.Arrays;

Addressquery addressquery = new Addressquery.Builder()
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

