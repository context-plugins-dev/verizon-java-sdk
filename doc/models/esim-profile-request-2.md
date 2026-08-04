
# ESIM Profile Request 2

## Structure

`ESIMProfileRequest2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Devices` | [`List<ESIMDeviceList>`](../../doc/models/esim-device-list.md) | Optional | **Constraints**: *Maximum Items*: `100` | List<ESIMDeviceList> getDevices() | setDevices(List<ESIMDeviceList> devices) |
| `AccountName` | `String` | Optional | - | String getAccountName() | setAccountName(String accountName) |
| `ServicePlan` | `String` | Optional | - | String getServicePlan() | setServicePlan(String servicePlan) |
| `MdnZipCode` | `String` | Optional | - | String getMdnZipCode() | setMdnZipCode(String mdnZipCode) |

## Example

```java
import com.verizon.thingspace.models.ESIMDeviceId;
import com.verizon.thingspace.models.ESIMDeviceList;
import com.verizon.thingspace.models.ESIMProfileRequest2;
import com.verizon.thingspace.models.containers.ESIMDeviceListDeviceIds;
import java.util.Arrays;

ESIMProfileRequest2 eSIMProfileRequest2 = new ESIMProfileRequest2.Builder()
    .devices(Arrays.asList(
        new ESIMDeviceList.Builder()
            .deviceIds(Arrays.asList(
                ESIMDeviceListDeviceIds.fromESIMDeviceId(
                    new ESIMDeviceId.Builder()
                        .id("id4")
                        .kind("kind2")
                        .build()
                )
            ))
            .build(),
        new ESIMDeviceList.Builder()
            .deviceIds(Arrays.asList(
                ESIMDeviceListDeviceIds.fromESIMDeviceId(
                    new ESIMDeviceId.Builder()
                        .id("id4")
                        .kind("kind2")
                        .build()
                )
            ))
            .build()
    ))
    .accountName("0000123456-00001")
    .servicePlan("The service plan name")
    .mdnZipCode("five digit zip code")
    .build();
```

