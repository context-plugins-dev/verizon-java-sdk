
# Carrier Activate Request

Request for carrier activation.

## Structure

`CarrierActivateRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Devices` | [`List<AccountDeviceList>`](../../doc/models/account-device-list.md) | Required | Up to 10,000 devices for which you want to activate service, specified by device identifier. | List<AccountDeviceList> getDevices() | setDevices(List<AccountDeviceList> devices) |
| `ServicePlan` | `String` | Required | The service plan code that you want to assign to all specified devices. | String getServicePlan() | setServicePlan(String servicePlan) |
| `MdnZipCode` | `String` | Required | The Zip code of the location where the line of service will primarily be used, or a Zip code that you have been told to use with these devices. For accounts that are configured for geographic numbering, this is the ZIP code from which the MDN will be derived. | String getMdnZipCode() | setMdnZipCode(String mdnZipCode) |
| `AccountName` | `String` | Optional | The name of a billing account. | String getAccountName() | setAccountName(String accountName) |
| `CarrierIpPoolName` | `String` | Optional | The private IP pool (Carrier Group Name) from which your device IP addresses will be derived. | String getCarrierIpPoolName() | setCarrierIpPoolName(String carrierIpPoolName) |
| `CarrierName` | `String` | Optional | The carrier that will perform the activation. | String getCarrierName() | setCarrierName(String carrierName) |
| `CostCenterCode` | `String` | Optional | A string to identify the cost center that the device is associated with. | String getCostCenterCode() | setCostCenterCode(String costCenterCode) |
| `CustomFields` | [`List<CustomFields>`](../../doc/models/custom-fields.md) | Optional | A user-defined descriptive field, limited to 50 characters. | List<CustomFields> getCustomFields() | setCustomFields(List<CustomFields> customFields) |
| `GroupName` | `String` | Optional | If you specify devices by ID in the devices parameters, this is the name of a device group that the devices should be added to.If you don't specify individual devices with the devices parameter, you can provide the name of a device group to activate all devices in that group. | String getGroupName() | setGroupName(String groupName) |
| `LeadId` | `String` | Optional | The ID of a “Qualified” or “Closed - Won” VPP customer lead, which is used with other values to determine MDN assignment, taxation, and compensation. | String getLeadId() | setLeadId(String leadId) |
| `PrimaryPlaceOfUse` | [`PlaceOfUse`](../../doc/models/place-of-use.md) | Optional | The customer name and the address of the device's primary place of use. Leave these fields empty to use the account profile address as the primary place of use. These values will be applied to all devices in the request.If the account is enabled for non-geographic MDNs and the device supports it, the primaryPlaceOfUse address will also be used to derive the MDN for the device. | PlaceOfUse getPrimaryPlaceOfUse() | setPrimaryPlaceOfUse(PlaceOfUse primaryPlaceOfUse) |
| `PublicIpRestriction` | `String` | Optional | For devices with static IP addresses on the public network, this specifies whether the devices have general access to the Internet. | String getPublicIpRestriction() | setPublicIpRestriction(String publicIpRestriction) |
| `SkuNumber` | `String` | Optional | The Stock Keeping Unit (SKU) of a 4G device type can be used with ICCID device identifiers in lieu of an IMEI when activating 4G devices. The SkuNumber will be used with all devices in the request, so all devices must be of the same type. | String getSkuNumber() | setSkuNumber(String skuNumber) |

## Example

```java
import com.verizon.thingspace.models.AccountDeviceList;
import com.verizon.thingspace.models.Address;
import com.verizon.thingspace.models.CarrierActivateRequest;
import com.verizon.thingspace.models.CustomFields;
import com.verizon.thingspace.models.CustomerName;
import com.verizon.thingspace.models.DeviceId;
import com.verizon.thingspace.models.PlaceOfUse;
import java.util.Arrays;

CarrierActivateRequest carrierActivateRequest = new CarrierActivateRequest.Builder(
    Arrays.asList(
        new AccountDeviceList.Builder(
            Arrays.asList(
                new DeviceId.Builder(
                    "990013907835573",
                    "imei"
                )
                .build(),
                new DeviceId.Builder(
                    "89141390780800784259",
                    "iccid"
                )
                .build()
            )
        )
        .ipaddress("ipAddress4")
        .build(),
        new AccountDeviceList.Builder(
            Arrays.asList(
                new DeviceId.Builder(
                    "990013907884259",
                    "imei"
                )
                .build(),
                new DeviceId.Builder(
                    "89141390780800735573",
                    "iccid"
                )
                .build()
            )
        )
        .ipaddress("ipAddress4")
        .build()
    ),
    "m2m_4G",
    "98801"
)
.accountName("0868924207-00001")
.carrierIpPoolName("carrierIpPoolName2")
.carrierName("carrierName6")
.costCenterCode("costCenterCode6")
.customFields(Arrays.asList(
        new CustomFields.Builder(
            "CustomField2"
        )
        .value("SuperVend")
        .build()
    ))
.groupName("4G West")
.primaryPlaceOfUse(new PlaceOfUse.Builder(
        new Address.Builder(
            "1600 Pennsylvania Ave NW",
            "Washington",
            "DC",
            "20500",
            "USA"
        )
        .build(),
        new CustomerName.Builder(
            "Zaffod",
            "Beeblebrox"
        )
        .title("President")
        .build()
    )
    .build())
.build();
```

