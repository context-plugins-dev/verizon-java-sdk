
# V2 Licenses Assigned Removed Result

License assignment or removal confirmation.

## Structure

`V2LicensesAssignedRemovedResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | Account name. | String getAccountName() | setAccountName(String accountName) |
| `LicTotalCount` | `int` | Required | Total license count. | int getLicTotalCount() | setLicTotalCount(int licTotalCount) |
| `LicUsedCount` | `int` | Required | Assigned license count. | int getLicUsedCount() | setLicUsedCount(int licUsedCount) |
| `DeviceList` | [`List<V2DeviceStatus>`](../../doc/models/v2-device-status.md) | Required | List of devices with id in IMEI. | List<V2DeviceStatus> getDeviceList() | setDeviceList(List<V2DeviceStatus> deviceList) |

## Example

```java
import com.verizon.thingspace.models.V2DeviceStatus;
import com.verizon.thingspace.models.V2LicensesAssignedRemovedResult;
import java.util.Arrays;

V2LicensesAssignedRemovedResult v2LicensesAssignedRemovedResult = new V2LicensesAssignedRemovedResult.Builder(
    "0242078689-00001",
    1000,
    502,
    Arrays.asList(
        new V2DeviceStatus.Builder(
            "990003425730524",
            "Success"
        )
        .resultReason("Success")
        .build(),
        new V2DeviceStatus.Builder(
            "990000473475967",
            "Failure"
        )
        .resultReason("Device does not exist.")
        .build()
    )
)
.build();
```

