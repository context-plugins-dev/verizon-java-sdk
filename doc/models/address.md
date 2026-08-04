
# Address

The customer address for the line's primary place of use, for line usage taxation.

## Structure

`Address`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AddressLine1` | `String` | Required | The street address for the line's primary place of use. This must be a physical address for taxation; it cannot be a P.O. box. | String getAddressLine1() | setAddressLine1(String addressLine1) |
| `AddressLine2` | `String` | Optional | Optional additional street address information. | String getAddressLine2() | setAddressLine2(String addressLine2) |
| `City` | `String` | Required | The city for the line's primary place of use. | String getCity() | setCity(String city) |
| `State` | `String` | Required | The state for the line's primary place of use. | String getState() | setState(String state) |
| `Zip` | `String` | Required | The ZIP code for the line's primary place of use. | String getZip() | setZip(String zip) |
| `Zip4` | `String` | Optional | The ZIP+4 for the line's primary place of use. | String getZip4() | setZip4(String zip4) |
| `Country` | `String` | Required | Either “US” or “USA” for the country of the line's primary place of use. | String getCountry() | setCountry(String country) |
| `Phone` | `String` | Optional | A phone number where the customer can be reached. | String getPhone() | setPhone(String phone) |
| `PhoneType` | `String` | Optional | A single letter to indicate the customer phone type. | String getPhoneType() | setPhoneType(String phoneType) |
| `EmailAddress` | `String` | Optional | An email address for the customer. | String getEmailAddress() | setEmailAddress(String emailAddress) |

## Example

```java
import com.verizon.thingspace.models.Address;

Address address = new Address.Builder(
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
.build();
```

