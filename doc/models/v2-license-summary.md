
# V2 License Summary

Summary of license assignment.

## Structure

`V2LicenseSummary`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | Account identifier. | String getAccountName() | setAccountName(String accountName) |
| `TotalLicense` | `Integer` | Optional | Total FOTA license count. | Integer getTotalLicense() | setTotalLicense(Integer totalLicense) |
| `AssignedLicenses` | `int` | Required | Assigned FOTA license count. | int getAssignedLicenses() | setAssignedLicenses(int assignedLicenses) |
| `HasMoreData` | `boolean` | Required | True if there are more devices to retrieve. | boolean getHasMoreData() | setHasMoreData(boolean hasMoreData) |
| `LastSeenDeviceId` | `String` | Optional | Last seen device identifier. | String getLastSeenDeviceId() | setLastSeenDeviceId(String lastSeenDeviceId) |
| `MaxPageSize` | `int` | Required | Maximum page size. | int getMaxPageSize() | setMaxPageSize(int maxPageSize) |
| `DeviceList` | [`List<V2LicenseDevice>`](../../doc/models/v2-license-device.md) | Optional | Device IMEI list. | List<V2LicenseDevice> getDeviceList() | setDeviceList(List<V2LicenseDevice> deviceList) |

## Example

```java
import com.verizon.thingspace.models.V2LicenseDevice;
import com.verizon.thingspace.models.V2LicenseSummary;
import java.util.Arrays;

V2LicenseSummary v2LicenseSummary = new V2LicenseSummary.Builder(
    "0402196254-00001",
    4319,
    true,
    10
)
.totalLicense(5000)
.lastSeenDeviceId("1000")
.deviceList(Arrays.asList(
        new V2LicenseDevice.Builder(
            "990003425730535"
        )
        .assignmentTime("2017-11-29T16:03:42.000Z")
        .build(),
        new V2LicenseDevice.Builder(
            "990000473475989"
        )
        .assignmentTime("2017-11-29T16:03:42.000Z")
        .build(),
        new V2LicenseDevice.Builder(
            "990000347475989"
        )
        .assignmentTime("2017-11-29T16:03:42.000Z")
        .build(),
        new V2LicenseDevice.Builder(
            "990007303425535"
        )
        .assignmentTime("2017-11-29T16:03:42.000Z")
        .build()
    ))
.build();
```

