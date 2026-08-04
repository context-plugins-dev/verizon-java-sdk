
# Deactivate Device Profile Request

## Structure

`DeactivateDeviceProfileRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | - | String getAccountName() | setAccountName(String accountName) |
| `ReasonCode` | `String` | Required | - | String getReasonCode() | setReasonCode(String reasonCode) |
| `Devices` | [`List<DeactivateDeviceList>`](../../doc/models/deactivate-device-list.md) | Optional | **Constraints**: *Maximum Items*: `100` | List<DeactivateDeviceList> getDevices() | setDevices(List<DeactivateDeviceList> devices) |
| `CarrierName` | `String` | Optional | - | String getCarrierName() | setCarrierName(String carrierName) |
| `EtfWaiver` | `Boolean` | Optional | **Default**: `true` | Boolean getEtfWaiver() | setEtfWaiver(Boolean etfWaiver) |
| `CheckFallbackProfile` | `Boolean` | Optional | **Default**: `false` | Boolean getCheckFallbackProfile() | setCheckFallbackProfile(Boolean checkFallbackProfile) |

## Example

```java
import com.verizon.thingspace.models.DeactivateDeviceList;
import com.verizon.thingspace.models.DeactivateDeviceProfileRequest;
import com.verizon.thingspace.models.DeviceId;
import com.verizon.thingspace.models.containers.DeactivateDeviceListIds;
import java.util.Arrays;

DeactivateDeviceProfileRequest deactivateDeviceProfileRequest = new DeactivateDeviceProfileRequest.Builder(
    "0000123456-00001",
    "a short code for the reason action was taken"
)
.devices(Arrays.asList(
        new DeactivateDeviceList.Builder()
            .ids(Arrays.asList(
                DeactivateDeviceListIds.fromDeviceId(
                    new DeviceId.Builder(
                        "id2",
                        "kind0"
                    )
                    .build()
                ),
                DeactivateDeviceListIds.fromDeviceId(
                    new DeviceId.Builder(
                        "id2",
                        "kind0"
                    )
                    .build()
                ),
                DeactivateDeviceListIds.fromDeviceId(
                    new DeviceId.Builder(
                        "id2",
                        "kind0"
                    )
                    .build()
                )
            ))
            .build(),
        new DeactivateDeviceList.Builder()
            .ids(Arrays.asList(
                DeactivateDeviceListIds.fromDeviceId(
                    new DeviceId.Builder(
                        "id2",
                        "kind0"
                    )
                    .build()
                ),
                DeactivateDeviceListIds.fromDeviceId(
                    new DeviceId.Builder(
                        "id2",
                        "kind0"
                    )
                    .build()
                ),
                DeactivateDeviceListIds.fromDeviceId(
                    new DeviceId.Builder(
                        "id2",
                        "kind0"
                    )
                    .build()
                )
            ))
            .build()
    ))
.carrierName("the name of the mobile service provider")
.etfWaiver(true)
.checkFallbackProfile(false)
.build();
```

