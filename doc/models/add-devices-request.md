
# Add Devices Request

Request to add the devices.

## Structure

`AddDevicesRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `State` | `String` | Required | The initial service state for the devices. The only valid state is “Pre-active.” | String getState() | setState(String state) |
| `DevicesToAdd` | [`List<AccountDeviceList>`](../../doc/models/account-device-list.md) | Required | The devices that you want to add. | List<AccountDeviceList> getDevicesToAdd() | setDevicesToAdd(List<AccountDeviceList> devicesToAdd) |
| `AccountName` | `String` | Optional | The billing account to which the devices are added. | String getAccountName() | setAccountName(String accountName) |
| `CustomFields` | [`List<CustomFields>`](../../doc/models/custom-fields.md) | Optional | The names and values for any custom fields that you want set for the devices as they are added to the account. | List<CustomFields> getCustomFields() | setCustomFields(List<CustomFields> customFields) |
| `GroupName` | `String` | Optional | The name of a device group to add the devices to. They are added to the default device group if you don't include this parameter. | String getGroupName() | setGroupName(String groupName) |
| `SkuNumber` | `String` | Optional | The Stock Keeping Unit (SKU) number of a 4G device type with an embedded SIM. | String getSkuNumber() | setSkuNumber(String skuNumber) |
| `SmsrOid` | `String` | Optional | **Constraints**: *Minimum Length*: `3`, *Maximum Length*: `32`, *Pattern*: `^[A-Za-z0-9]{3,32}$` | String getSmsrOid() | setSmsrOid(String smsrOid) |

## Example

```java
import com.verizon.thingspace.models.AccountDeviceList;
import com.verizon.thingspace.models.AddDevicesRequest;
import com.verizon.thingspace.models.CustomFields;
import com.verizon.thingspace.models.DeviceId;
import java.util.Arrays;

AddDevicesRequest addDevicesRequest = new AddDevicesRequest.Builder(
    "Pre-active",
    Arrays.asList(
        new AccountDeviceList.Builder(
            Arrays.asList(
                new DeviceId.Builder(
                    "15-digit IMEI",
                    "imei"
                )
                .build(),
                new DeviceId.Builder(
                    "20-digit ICCID",
                    "iccid"
                )
                .build()
            )
        )
        .ipaddress("ipAddress2")
        .build(),
        new AccountDeviceList.Builder(
            Arrays.asList(
                new DeviceId.Builder(
                    "15-digit IMEI",
                    "imei"
                )
                .build(),
                new DeviceId.Builder(
                    "20-digit ICCID",
                    "iccid"
                )
                .build()
            )
        )
        .ipaddress("ipAddress2")
        .build()
    )
)
.accountName("0000123456-00001")
.customFields(Arrays.asList(
        new CustomFields.Builder(
            "CustomField2"
        )
        .value("SuperVend")
        .build()
    ))
.groupName("West Region")
.skuNumber("skuNumber4")
.smsrOid("smsrOid8")
.build();
```

