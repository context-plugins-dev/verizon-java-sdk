
# Retrieve Monitors Request

## Structure

`RetrieveMonitorsRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | The name of a billing account. | String getAccountName() | setAccountName(String accountName) |
| `Devices` | [`List<AccountDeviceList>`](../../doc/models/account-device-list.md) | Required | The devices for which you want to restore service, specified by device identifier. | List<AccountDeviceList> getDevices() | setDevices(List<AccountDeviceList> devices) |
| `MonitorType` | `String` | Optional | The name of a billing account. | String getMonitorType() | setMonitorType(String monitorType) |

## Example

```java
import com.verizon.thingspace.models.AccountDeviceList;
import com.verizon.thingspace.models.DeviceId;
import com.verizon.thingspace.models.RetrieveMonitorsRequest;
import java.util.Arrays;

RetrieveMonitorsRequest retrieveMonitorsRequest = new RetrieveMonitorsRequest.Builder(
    "0868924207-00001",
    Arrays.asList(
        new AccountDeviceList.Builder(
            Arrays.asList(
                new DeviceId.Builder(
                    "89148000000800139708",
                    "iccid"
                )
                .build()
            )
        )
        .ipaddress("ipAddress4")
        .build()
    )
)
.monitorType("monitorType")
.build();
```

