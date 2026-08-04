
# Fall Back

## Structure

`FallBack`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Devices` | [`List<List<FallBackDevices>>`](../../doc/models/containers/fall-back-devices.md) | Optional | This is 2d List of a container for any-of cases.<br><br>**Constraints**: *Maximum Items*: `100` | List<List<FallBackDevices>> getDevices() | setDevices(List<List<FallBackDevices>> devices) |
| `AccountName` | `String` | Optional | The numeric name of the account, in the format "0000123456-00001". Leading zeros must be included.<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `32`, *Pattern*: `^[0-9]{3,32}$` | String getAccountName() | setAccountName(String accountName) |

## Example

```java
import com.verizon.thingspace.models.DeviceIdarray;
import com.verizon.thingspace.models.FallBack;
import com.verizon.thingspace.models.containers.FallBackDevices;
import java.util.Arrays;

FallBack fallBack = new FallBack.Builder()
    .devices(Arrays.asList(
        Arrays.asList(
            FallBackDevices.fromListOfDeviceIdarray(
                Arrays.asList(
                    new DeviceIdarray.Builder()
                        .kind("kind6")
                        .id("id8")
                        .build(),
                    new DeviceIdarray.Builder()
                        .kind("kind6")
                        .id("id8")
                        .build()
                )
            ),
            FallBackDevices.fromListOfDeviceIdarray(
                Arrays.asList(
                    new DeviceIdarray.Builder()
                        .kind("kind6")
                        .id("id8")
                        .build(),
                    new DeviceIdarray.Builder()
                        .kind("kind6")
                        .id("id8")
                        .build(),
                    new DeviceIdarray.Builder()
                        .kind("kind6")
                        .id("id8")
                        .build()
                )
            )
        ),
        Arrays.asList(
            FallBackDevices.fromListOfDeviceIdarray(
                Arrays.asList(
                    new DeviceIdarray.Builder()
                        .kind("kind6")
                        .id("id8")
                        .build(),
                    new DeviceIdarray.Builder()
                        .kind("kind6")
                        .id("id8")
                        .build()
                )
            ),
            FallBackDevices.fromListOfDeviceIdarray(
                Arrays.asList(
                    new DeviceIdarray.Builder()
                        .kind("kind6")
                        .id("id8")
                        .build(),
                    new DeviceIdarray.Builder()
                        .kind("kind6")
                        .id("id8")
                        .build(),
                    new DeviceIdarray.Builder()
                        .kind("kind6")
                        .id("id8")
                        .build()
                )
            )
        )
    ))
    .accountName("accountName4")
    .build();
```

