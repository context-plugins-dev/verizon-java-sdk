
# M5 G Bidevice Detailsresponse

## Structure

`M5gBideviceDetailsresponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `HasMoreData` | `Boolean` | Optional | - | Boolean getHasMoreData() | setHasMoreData(Boolean hasMoreData) |
| `Devices` | [`List<M5gBideviceDetailsresponseDevices>`](../../doc/models/containers/m5-g-bidevice-detailsresponse-devices.md) | Optional | This is List of a container for any-of cases. | List<M5gBideviceDetailsresponseDevices> getDevices() | setDevices(List<M5gBideviceDetailsresponseDevices> devices) |

## Example

```java
import com.verizon.thingspace.models.M5gBiCarrierInformation;
import com.verizon.thingspace.models.M5gBiaccountNameobject;
import com.verizon.thingspace.models.M5gBideviceDetailsresponse;
import com.verizon.thingspace.models.containers.M5gBideviceDetailsresponseDevices;
import java.util.Arrays;

M5gBideviceDetailsresponse m5gBideviceDetailsresponse = new M5gBideviceDetailsresponse.Builder()
    .hasMoreData(false)
    .devices(Arrays.asList(
        M5gBideviceDetailsresponseDevices.fromM5gBiaccountNameobject(
            new M5gBiaccountNameobject.Builder()
                .accountName("accountName0")
                .billingCycleEndDate("billingCycleEndDate6")
                .carrierInformation(Arrays.asList(
                    new M5gBiCarrierInformation.Builder()
                        .carrierName("carrierName4")
                        .build(),
                    new M5gBiCarrierInformation.Builder()
                        .carrierName("carrierName4")
                        .build(),
                    new M5gBiCarrierInformation.Builder()
                        .carrierName("carrierName4")
                        .build()
                ))
                .connected(false)
                .createdAt("createdAt0")
                .build()
        ),
        M5gBideviceDetailsresponseDevices.fromM5gBiaccountNameobject(
            new M5gBiaccountNameobject.Builder()
                .accountName("accountName0")
                .billingCycleEndDate("billingCycleEndDate6")
                .carrierInformation(Arrays.asList(
                    new M5gBiCarrierInformation.Builder()
                        .carrierName("carrierName4")
                        .build(),
                    new M5gBiCarrierInformation.Builder()
                        .carrierName("carrierName4")
                        .build(),
                    new M5gBiCarrierInformation.Builder()
                        .carrierName("carrierName4")
                        .build()
                ))
                .connected(false)
                .createdAt("createdAt0")
                .build()
        )
    ))
    .build();
```

