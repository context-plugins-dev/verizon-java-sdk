
# Account Device List Result

Response for a request to list down account devices.

## Structure

`AccountDeviceListResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Devices` | [`List<ThingspaceDevice>`](../../doc/models/thingspace-device.md) | Optional | Up to 10,000 devices that you want to move to a different account, specified by device identifier. | List<ThingspaceDevice> getDevices() | setDevices(List<ThingspaceDevice> devices) |
| `HasMoreData` | `Boolean` | Optional | False for a status 200 response.True for a status 202 response, indicating that there is more data to be retrieved. | Boolean getHasMoreData() | setHasMoreData(Boolean hasMoreData) |

## Example

```java
import com.verizon.thingspace.models.AccountDeviceListResult;
import com.verizon.thingspace.models.CarrierInformation;
import com.verizon.thingspace.models.DeviceId;
import com.verizon.thingspace.models.ThingspaceDevice;
import java.util.Arrays;

AccountDeviceListResult accountDeviceListResult = new AccountDeviceListResult.Builder()
    .devices(Arrays.asList(
        new ThingspaceDevice.Builder()
            .accountName("0000123456-00001")
            .billingCycleEndDate("2020-05-09T20:00:00-04:00")
            .carrierInformations(Arrays.asList(
                new CarrierInformation.Builder()
                    .carrierName("Verizon Wireless")
                    .servicePlan("m2m4G")
                    .state("active")
                    .build()
            ))
            .connected(false)
            .createdAt("2019-08-07T10:42:15-04:00")
            .deviceIds(Arrays.asList(
                new DeviceId.Builder(
                    "10-digit MDN",
                    "mdn"
                )
                .build(),
                new DeviceId.Builder(
                    "15-digit IMEI",
                    "imei"
                )
                .build()
            ))
            .groupNames(Arrays.asList(
                "southwest"
            ))
            .ipaddress("0.0.0.0")
            .lastActivationBy("Joe Q Public")
            .lastActivationDate("2019-08-07T10:42:34-04:00")
            .lastConnectionDate("2020-03-12T04:23:37-04:00")
            .build()
    ))
    .hasMoreData(false)
    .build();
```

