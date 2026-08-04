
# Account License Device List Item

The list of devices that have licenses assigned, including the date and time of when each license was assigned.

## Structure

`AccountLicenseDeviceListItem`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceId` | `String` | Optional | Device IMEI. | String getDeviceId() | setDeviceId(String deviceId) |
| `AssignmentTime` | `LocalDateTime` | Optional | Timestamp of when a license was assigned to the device. | LocalDateTime getAssignmentTime() | setAssignmentTime(LocalDateTime assignmentTime) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.AccountLicenseDeviceListItem;

AccountLicenseDeviceListItem accountLicenseDeviceListItem = new AccountLicenseDeviceListItem.Builder()
    .deviceId("990003425730535")
    .assignmentTime(DateTimeHelper.fromRfc8601DateTime("2017-11-29T16:03:42.000Z"))
    .build();
```

