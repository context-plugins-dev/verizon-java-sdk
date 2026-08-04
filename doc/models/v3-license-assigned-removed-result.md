
# V3 License Assigned Removed Result

License assignment/removal response.

## Structure

`V3LicenseAssignedRemovedResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | Account name. | String getAccountName() | setAccountName(String accountName) |
| `LicCount` | `int` | Required | Total license count. | int getLicCount() | setLicCount(int licCount) |
| `LicUsedCount` | `int` | Required | Assigned license count. | int getLicUsedCount() | setLicUsedCount(int licUsedCount) |
| `DeviceList` | [`List<V3DeviceStatus>`](../../doc/models/v3-device-status.md) | Required | List of devices with id in IMEI. | List<V3DeviceStatus> getDeviceList() | setDeviceList(List<V3DeviceStatus> deviceList) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.V3DeviceStatus;
import com.verizon.thingspace.models.V3LicenseAssignedRemovedResult;
import java.util.Arrays;

V3LicenseAssignedRemovedResult v3LicenseAssignedRemovedResult = new V3LicenseAssignedRemovedResult.Builder(
    "0000123456-00001",
    1000,
    2,
    Arrays.asList(
        new V3DeviceStatus.Builder(
            "15-digit IMEI",
            "UpgradePending"
        )
        .resultReason("Upgrade pending, the device upgrade is estimated to be scheduled for 06 Oct 22 18:05 UTC")
        .updatedTime(DateTimeHelper.fromRfc8601DateTime("2022-08-05T21:05:27.129Z"))
        .recentAttemptTime(DateTimeHelper.fromRfc8601DateTime("2022-10-05T21:05:01.19Z"))
        .nextAttemptTime(DateTimeHelper.fromRfc8601DateTime("2022-10-06T18:35:00Z"))
        .build()
    )
)
.build();
```

