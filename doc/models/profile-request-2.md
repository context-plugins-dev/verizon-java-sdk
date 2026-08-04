
# Profile Request 2

## Structure

`ProfileRequest2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Devices` | [`List<DeviceList2>`](../../doc/models/device-list-2.md) | Optional | **Constraints**: *Maximum Items*: `100` | List<DeviceList2> getDevices() | setDevices(List<DeviceList2> devices) |
| `AccountName` | `String` | Optional | - | String getAccountName() | setAccountName(String accountName) |
| `CarrierName` | `String` | Optional | - | String getCarrierName() | setCarrierName(String carrierName) |
| `ReasonCode` | `String` | Optional | - | String getReasonCode() | setReasonCode(String reasonCode) |
| `EtfWaiver` | `Boolean` | Optional | **Default**: `true` | Boolean getEtfWaiver() | setEtfWaiver(Boolean etfWaiver) |
| `CheckFallbackProfile` | `Boolean` | Optional | **Default**: `false` | Boolean getCheckFallbackProfile() | setCheckFallbackProfile(Boolean checkFallbackProfile) |

## Example

```java
import com.verizon.thingspace.models.DeviceList2;
import com.verizon.thingspace.models.ESIMDeviceId;
import com.verizon.thingspace.models.ProfileRequest2;
import com.verizon.thingspace.models.containers.DeviceList2Ids;
import java.util.Arrays;

ProfileRequest2 profileRequest2 = new ProfileRequest2.Builder()
    .devices(Arrays.asList(
        new DeviceList2.Builder()
            .ids(Arrays.asList(
                DeviceList2Ids.fromESIMDeviceId(
                    new ESIMDeviceId.Builder()
                        .id("id4")
                        .kind("kind2")
                        .build()
                ),
                DeviceList2Ids.fromESIMDeviceId(
                    new ESIMDeviceId.Builder()
                        .id("id4")
                        .kind("kind2")
                        .build()
                ),
                DeviceList2Ids.fromESIMDeviceId(
                    new ESIMDeviceId.Builder()
                        .id("id4")
                        .kind("kind2")
                        .build()
                )
            ))
            .build(),
        new DeviceList2.Builder()
            .ids(Arrays.asList(
                DeviceList2Ids.fromESIMDeviceId(
                    new ESIMDeviceId.Builder()
                        .id("id4")
                        .kind("kind2")
                        .build()
                ),
                DeviceList2Ids.fromESIMDeviceId(
                    new ESIMDeviceId.Builder()
                        .id("id4")
                        .kind("kind2")
                        .build()
                ),
                DeviceList2Ids.fromESIMDeviceId(
                    new ESIMDeviceId.Builder()
                        .id("id4")
                        .kind("kind2")
                        .build()
                )
            ))
            .build()
    ))
    .accountName("0000123456-00001")
    .carrierName("Verizon Wireless")
    .reasonCode("FF")
    .etfWaiver(true)
    .checkFallbackProfile(false)
    .build();
```

