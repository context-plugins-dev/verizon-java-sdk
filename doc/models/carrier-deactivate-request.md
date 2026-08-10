
# Carrier Deactivate Request

Request to deactivate a carrier.

## Structure

`CarrierDeactivateRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | The name of a billing account. | String getAccountName() | setAccountName(String accountName) |
| `Devices` | [`List<AccountDeviceList>`](../../doc/models/account-device-list.md) | Required | The devices for which you want to deactivate service, specified by device identifier. | List<AccountDeviceList> getDevices() | setDevices(List<AccountDeviceList> devices) |
| `ReasonCode` | `String` | Required | Code identifying the reason for the deactivation. Currently the only valid reason code is “FF”, which corresponds to General Admin/Maintenance. | String getReasonCode() | setReasonCode(String reasonCode) |
| `CustomFields` | [`List<CustomFields>`](../../doc/models/custom-fields.md) | Optional | Custom field names and values, if you want to only include devices that have matching values. | List<CustomFields> getCustomFields() | setCustomFields(List<CustomFields> customFields) |
| `EtfWaiver` | `Boolean` | Optional | Fees may be assessed for deactivating Verizon Wireless devices, depending on the account contract. The etfWaiver parameter waives the Early Termination Fee (ETF), if applicable. | Boolean getEtfWaiver() | setEtfWaiver(Boolean etfWaiver) |
| `GroupName` | `String` | Optional | The name of a device group, if you want to deactivate all devices in that group. | String getGroupName() | setGroupName(String groupName) |
| `ServicePlan` | `String` | Optional | The name of a service plan, if you want to only include devices that have that service plan. | String getServicePlan() | setServicePlan(String servicePlan) |
| `DeleteAfterDeactivation` | `Boolean` | Optional | - | Boolean getDeleteAfterDeactivation() | setDeleteAfterDeactivation(Boolean deleteAfterDeactivation) |

## Example

```java
import com.verizon.thingspace.models.AccountDeviceList;
import com.verizon.thingspace.models.CarrierDeactivateRequest;
import com.verizon.thingspace.models.CustomFields;
import com.verizon.thingspace.models.DeviceId;
import java.util.Arrays;

CarrierDeactivateRequest carrierDeactivateRequest = new CarrierDeactivateRequest.Builder(
    "0000123456-00001",
    Arrays.asList(
        new AccountDeviceList.Builder(
            Arrays.asList(
                new DeviceId.Builder(
                    "20-digit ICCID",
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
                    "20-digit ICCID",
                    "iccid"
                )
                .build()
            )
        )
        .ipaddress("ipAddress4")
        .build()
    ),
    "FF"
)
.customFields(Arrays.asList(
        new CustomFields.Builder(
            "key0"
        )
        .value("value2")
        .build(),
        new CustomFields.Builder(
            "key0"
        )
        .value("value2")
        .build()
    ))
.etfWaiver(true)
.groupName("groupName6")
.servicePlan("servicePlan4")
.deleteAfterDeactivation(false)
.build();
```

