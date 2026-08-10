
# Service Plan Update Request

Request to update service plan.

## Structure

`ServicePlanUpdateRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ServicePlan` | `String` | Required | The service plan code that you want to assign to all specified devices. | String getServicePlan() | setServicePlan(String servicePlan) |
| `AccountName` | `String` | Optional | The name of a billing account. | String getAccountName() | setAccountName(String accountName) |
| `CurrentServicePlan` | `String` | Optional | The name of a service plan, if you want to only include devices that have that service plan. | String getCurrentServicePlan() | setCurrentServicePlan(String currentServicePlan) |
| `CustomFields` | [`List<CustomFields>`](../../doc/models/custom-fields.md) | Optional | Custom field names and values, if you want to only include devices that have matching values. | List<CustomFields> getCustomFields() | setCustomFields(List<CustomFields> customFields) |
| `Devices` | [`List<AccountDeviceList>`](../../doc/models/account-device-list.md) | Optional | A list of the devices that you want to change, specified by device identifier. | List<AccountDeviceList> getDevices() | setDevices(List<AccountDeviceList> devices) |
| `GroupName` | `String` | Optional | The name of a device group, if you want to restore service for all devices in that group. | String getGroupName() | setGroupName(String groupName) |
| `CarrierIpPoolName` | `String` | Optional | **Constraints**: *Minimum Length*: `3`, *Maximum Length*: `32`, *Pattern*: `^[A-Za-z0-9]{3,32}$` | String getCarrierIpPoolName() | setCarrierIpPoolName(String carrierIpPoolName) |
| `TakeEffect` | `LocalDateTime` | Optional | - | LocalDateTime getTakeEffect() | setTakeEffect(LocalDateTime takeEffect) |

## Example

```java
import com.verizon.thingspace.models.AccountDeviceList;
import com.verizon.thingspace.models.CustomFields;
import com.verizon.thingspace.models.DeviceId;
import com.verizon.thingspace.models.ServicePlanUpdateRequest;
import java.util.Arrays;

ServicePlanUpdateRequest servicePlanUpdateRequest = new ServicePlanUpdateRequest.Builder(
    "new_service_plan_code"
)
.accountName("accountName8")
.currentServicePlan("currentServicePlan0")
.customFields(Arrays.asList(
        new CustomFields.Builder(
            "key0"
        )
        .value("value2")
        .build()
    ))
.devices(Arrays.asList(
        new AccountDeviceList.Builder(
            Arrays.asList(
                new DeviceId.Builder(
                    "A100003685E561",
                    "meid"
                )
                .build()
            )
        )
        .ipaddress("ipAddress4")
        .build()
    ))
.groupName("groupName6")
.build();
```

