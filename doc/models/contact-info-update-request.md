
# Contact Info Update Request

Request to update contact information.

## Structure

`ContactInfoUpdateRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `PrimaryPlaceOfUse` | [`PlaceOfUse`](../../doc/models/place-of-use.md) | Required | The customer name and the address of the device's primary place of use. Leave these fields empty to use the account profile address as the primary place of use. These values will be applied to all devices in the request.If the account is enabled for non-geographic MDNs and the device supports it, the primaryPlaceOfUse address will also be used to derive the MDN for the device. | PlaceOfUse getPrimaryPlaceOfUse() | setPrimaryPlaceOfUse(PlaceOfUse primaryPlaceOfUse) |
| `AccountName` | `String` | Optional | The name of the billing account that the devices belong to. An account name is usually numeric, and must include any leading zeros. | String getAccountName() | setAccountName(String accountName) |
| `Devices` | [`List<AccountDeviceList>`](../../doc/models/account-device-list.md) | Optional | A list of the devices that you want to change, specified by device identifier. You only need to provide one identifier per device. Do not include accountName, groupName, customFields, or servicePlan if you use this parameter. | List<AccountDeviceList> getDevices() | setDevices(List<AccountDeviceList> devices) |

## Example

```java
import com.verizon.thingspace.models.AccountDeviceList;
import com.verizon.thingspace.models.Address;
import com.verizon.thingspace.models.ContactInfoUpdateRequest;
import com.verizon.thingspace.models.CustomerName;
import com.verizon.thingspace.models.DeviceId;
import com.verizon.thingspace.models.PlaceOfUse;
import java.util.Arrays;

ContactInfoUpdateRequest contactInfoUpdateRequest = new ContactInfoUpdateRequest.Builder(
    new PlaceOfUse.Builder(
        new Address.Builder(
            "9868 Scranton Rd",
            "San Diego",
            "CA",
            "92121",
            "USA"
        )
        .addressLine2("Suite A")
        .zip4("0001")
        .phone("1234567890")
        .phoneType("H")
        .emailAddress("zaffod@theinternet.com")
        .build(),
        new CustomerName.Builder(
            "Zaffod",
            "Beeblebrox"
        )
        .title("President")
        .middleName("P")
        .suffix("I")
        .build()
    )
    .build()
)
.accountName("0212345678-00001")
.devices(Arrays.asList(
        new AccountDeviceList.Builder(
            Arrays.asList(
                new DeviceId.Builder(
                    "19110173057",
                    "ESN"
                )
                .build(),
                new DeviceId.Builder(
                    "19110173057",
                    "ESN"
                )
                .build()
            )
        )
        .ipaddress("ipAddress4")
        .build()
    ))
.build();
```

