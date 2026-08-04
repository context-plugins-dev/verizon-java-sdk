
# Get Device List with Profiles Request

## Structure

`GetDeviceListWithProfilesRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | **Constraints**: *Minimum Length*: `3`, *Maximum Length*: `32`, *Pattern*: `^[A-Za-z0-9\-]{3,32}$` | String getAccountName() | setAccountName(String accountName) |
| `ProvisioningStatusFilter` | `String` | Optional | **Constraints**: *Minimum Length*: `3`, *Maximum Length*: `32`, *Pattern*: `^[A-Za-z0-9]{3,32}$` | String getProvisioningStatusFilter() | setProvisioningStatusFilter(String provisioningStatusFilter) |
| `ProfileStatusFilter` | `String` | Optional | **Constraints**: *Minimum Length*: `3`, *Maximum Length*: `32`, *Pattern*: `^[A-Za-z0-9]{3,32}$` | String getProfileStatusFilter() | setProfileStatusFilter(String profileStatusFilter) |
| `CarrierNameFilter` | `String` | Optional | **Constraints**: *Minimum Length*: `3`, *Maximum Length*: `32`, *Pattern*: `^[A-Za-z0-9]{3,32}$` | String getCarrierNameFilter() | setCarrierNameFilter(String carrierNameFilter) |
| `DeviceFilter` | [`List<GIODeviceId>`](../../doc/models/gio-device-id.md) | Optional | **Constraints**: *Maximum Items*: `50` | List<GIODeviceId> getDeviceFilter() | setDeviceFilter(List<GIODeviceId> deviceFilter) |

## Example

```java
import com.verizon.thingspace.models.GIODeviceId;
import com.verizon.thingspace.models.GetDeviceListWithProfilesRequest;
import java.util.Arrays;

GetDeviceListWithProfilesRequest getDeviceListWithProfilesRequest = new GetDeviceListWithProfilesRequest.Builder(
    "0000123456-00001"
)
.provisioningStatusFilter("ACTIVE")
.profileStatusFilter("UNKNOWN")
.carrierNameFilter("carrierNameFilter4")
.deviceFilter(Arrays.asList(
        new GIODeviceId.Builder(
            "kind2",
            "id4"
        )
        .build(),
        new GIODeviceId.Builder(
            "kind2",
            "id4"
        )
        .build(),
        new GIODeviceId.Builder(
            "kind2",
            "id4"
        )
        .build()
    ))
.build();
```

