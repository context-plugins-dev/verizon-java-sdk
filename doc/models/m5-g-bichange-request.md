
# M5 G Bichange Request

## Structure

`M5gBichangeRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Optional | - | String getAccountName() | setAccountName(String accountName) |
| `ServicePlan` | `String` | Optional | - | String getServicePlan() | setServicePlan(String servicePlan) |
| `DeviceListWithServiceAddress` | [`List<M5gBichangeRequestDeviceListWithServiceAddress>`](../../doc/models/containers/m5-g-bichange-request-device-list-with-service-address.md) | Optional | This is List of a container for any-of cases. | List<M5gBichangeRequestDeviceListWithServiceAddress> getDeviceListWithServiceAddress() | setDeviceListWithServiceAddress(List<M5gBichangeRequestDeviceListWithServiceAddress> deviceListWithServiceAddress) |
| `CurrentServicePlan` | `String` | Optional | - | String getCurrentServicePlan() | setCurrentServicePlan(String currentServicePlan) |

## Example

```java
import com.verizon.thingspace.models.M5gBichangeRequest;
import com.verizon.thingspace.models.M5gBideviceId1;
import com.verizon.thingspace.models.M5gBideviceIdarray2;
import com.verizon.thingspace.models.containers.M5gBichangeRequestDeviceListWithServiceAddress;
import java.util.Arrays;

M5gBichangeRequest m5gBichangeRequest = new M5gBichangeRequest.Builder()
    .accountName("0000123456-00001")
    .servicePlan("5G BI service plan name being changed to")
    .deviceListWithServiceAddress(Arrays.asList(
        M5gBichangeRequestDeviceListWithServiceAddress.fromM5gBideviceIdarray2(
            new M5gBideviceIdarray2.Builder()
                .deviceId(Arrays.asList(
                    new M5gBideviceId1.Builder()
                        .id("id0")
                        .kind("kind8")
                        .build(),
                    new M5gBideviceId1.Builder()
                        .id("id0")
                        .kind("kind8")
                        .build()
                ))
                .build()
        )
    ))
    .currentServicePlan("Optional name of the plan being changed from")
    .build();
```

