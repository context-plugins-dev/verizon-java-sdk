
# V3 License Summary

Information for FOTA licenses assigned to devices.

## Structure

`V3LicenseSummary`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | Account identifier. | String getAccountName() | setAccountName(String accountName) |
| `TotalLicenses` | `Integer` | Optional | Total FOTA license count. | Integer getTotalLicenses() | setTotalLicenses(Integer totalLicenses) |
| `AssignedLicenses` | `int` | Required | Assigned FOTA license count. | int getAssignedLicenses() | setAssignedLicenses(int assignedLicenses) |
| `HasMoreData` | `boolean` | Required | True if there are more devices to retrieve. | boolean getHasMoreData() | setHasMoreData(boolean hasMoreData) |
| `LastSeenDeviceId` | `String` | Optional | Last seen device identifier. | String getLastSeenDeviceId() | setLastSeenDeviceId(String lastSeenDeviceId) |
| `MaxPageSize` | `int` | Required | Maximum page size. | int getMaxPageSize() | setMaxPageSize(int maxPageSize) |
| `DeviceList` | [`List<V3LicenseDevice>`](../../doc/models/v3-license-device.md) | Optional | Device IMEI list. | List<V3LicenseDevice> getDeviceList() | setDeviceList(List<V3LicenseDevice> deviceList) |

## Example

```java
import com.verizon.thingspace.models.V3LicenseDevice;
import com.verizon.thingspace.models.V3LicenseSummary;
import java.util.Arrays;

V3LicenseSummary v3LicenseSummary = new V3LicenseSummary.Builder(
    "0000123456-00001",
    4319,
    true,
    1000
)
.totalLicenses(5000)
.lastSeenDeviceId("1000")
.deviceList(Arrays.asList(
        new V3LicenseDevice.Builder(
            "15-digit IMEI"
        )
        .assignmentTime("2017-11-29 20:15:42.738 +0000 UTC")
        .build(),
        new V3LicenseDevice.Builder(
            "15-digit IMEI"
        )
        .assignmentTime("2017-11-29 20:15:42.738 +0000 UTC")
        .build()
    ))
.build();
```

