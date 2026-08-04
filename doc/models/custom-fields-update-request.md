
# Custom Fields Update Request

Request to assign or change custom field values for one or more devices.

## Structure

`CustomFieldsUpdateRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Optional | The name of a billing account.This parameter is only required if the UWS account used for the current API session has access to multiple billing accounts.An account name is usually numeric, and must include any leading zeros. | String getAccountName() | setAccountName(String accountName) |
| `CustomFields` | [`List<CustomFields>`](../../doc/models/custom-fields.md) | Optional | Custom field names and values, if you want to only include devices that have matching values. | List<CustomFields> getCustomFields() | setCustomFields(List<CustomFields> customFields) |
| `CustomFieldsToUpdate` | [`List<CustomFields>`](../../doc/models/custom-fields.md) | Optional | The names and new values of any custom fields that you want to change. | List<CustomFields> getCustomFieldsToUpdate() | setCustomFieldsToUpdate(List<CustomFields> customFieldsToUpdate) |
| `Devices` | [`List<AccountDeviceList>`](../../doc/models/account-device-list.md) | Optional | The devices that you want to change. | List<AccountDeviceList> getDevices() | setDevices(List<AccountDeviceList> devices) |
| `GroupName` | `String` | Optional | The name of a device group, if you want to only include devices in that group. | String getGroupName() | setGroupName(String groupName) |
| `ServicePlan` | `String` | Optional | The name of a service plan, if you want to only include devices that have that service plan. | String getServicePlan() | setServicePlan(String servicePlan) |

## Example

```java
import com.verizon.thingspace.models.AccountDeviceList;
import com.verizon.thingspace.models.CustomFields;
import com.verizon.thingspace.models.CustomFieldsUpdateRequest;
import com.verizon.thingspace.models.DeviceId;
import java.util.Arrays;

CustomFieldsUpdateRequest customFieldsUpdateRequest = new CustomFieldsUpdateRequest.Builder()
    .accountName("accountName2")
    .customFields(Arrays.asList(
        null,
        new CustomFields.Builder(
            null,
            null
        )
        .build(),
        new CustomFields.Builder(
            null,
            null
        )
        .build()
    ))
    .customFieldsToUpdate(Arrays.asList(
        new CustomFields.Builder(
            "CustomField1",
            "West Region"
        )
        .build(),
        new CustomFields.Builder(
            "CustomField2",
            "Distribution"
        )
        .build()
    ))
    .devices(Arrays.asList(
        new AccountDeviceList.Builder(
            Arrays.asList(
                new DeviceId.Builder(
                    "89148000000800139708",
                    "iccid"
                )
                .build()
            )
        )
        .ipaddress("ipAddress4")
        .build()
    ))
    .groupName("groupName2")
    .build();
```

