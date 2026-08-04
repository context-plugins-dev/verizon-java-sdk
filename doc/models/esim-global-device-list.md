
# ESIM Global Device List

## Structure

`ESIMGlobalDeviceList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Optional | The numeric name of the account. | String getAccountName() | setAccountName(String accountName) |
| `ProvisioningStatusFilter` | [`ProvisioningStatusFilterEnum`](../../doc/models/provisioning-status-filter-enum.md) | Optional | The last status of the device as a list filter. | ProvisioningStatusFilterEnum getProvisioningStatusFilter() | setProvisioningStatusFilter(ProvisioningStatusFilterEnum provisioningStatusFilter) |
| `ProfileStatusFilter` | [`ProfileStatusFilterEnum`](../../doc/models/profile-status-filter-enum.md) | Optional | The last status of the device's profile as a filter. | ProfileStatusFilterEnum getProfileStatusFilter() | setProfileStatusFilter(ProfileStatusFilterEnum profileStatusFilter) |
| `CarrierNameFilter` | `String` | Optional | The cellular service provider. | String getCarrierNameFilter() | setCarrierNameFilter(String carrierNameFilter) |
| `DeviceFilter` | [`List<ESIMGlobalDeviceListDeviceFilter>`](../../doc/models/containers/esim-global-device-list-device-filter.md) | Optional | This is List of a container for any-of cases. | List<ESIMGlobalDeviceListDeviceFilter> getDeviceFilter() | setDeviceFilter(List<ESIMGlobalDeviceListDeviceFilter> deviceFilter) |

## Example

```java
import com.verizon.thingspace.models.ESIMDeviceId;
import com.verizon.thingspace.models.ESIMGlobalDeviceList;
import com.verizon.thingspace.models.ProfileStatusFilterEnum;
import com.verizon.thingspace.models.ProvisioningStatusFilterEnum;
import com.verizon.thingspace.models.containers.ESIMGlobalDeviceListDeviceFilter;
import java.util.Arrays;

ESIMGlobalDeviceList eSIMGlobalDeviceList = new ESIMGlobalDeviceList.Builder()
    .accountName("0000123456-00001")
    .provisioningStatusFilter(ProvisioningStatusFilterEnum.SUSPEND)
    .profileStatusFilter(ProfileStatusFilterEnum.DELETE)
    .carrierNameFilter("VerizonWireless")
    .deviceFilter(Arrays.asList(
        ESIMGlobalDeviceListDeviceFilter.fromESIMDeviceId(
            new ESIMDeviceId.Builder()
                .id("id4")
                .kind("kind2")
                .build()
        )
    ))
    .build();
```

