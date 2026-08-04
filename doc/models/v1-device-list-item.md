
# V1 Device List Item

A JSON object for each device that was included in the request, showing the device IMEI, the status of the addition or removal, and additional information about the status.

## Structure

`V1DeviceListItem`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceId` | `String` | Optional | Device IMEI. | String getDeviceId() | setDeviceId(String deviceId) |
| `Status` | `String` | Optional | Whether the device was successfully added or removed from the campaign. | String getStatus() | setStatus(String status) |
| `Reason` | `String` | Optional | Additional details about the status. | String getReason() | setReason(String reason) |

## Example

```java
import com.verizon.thingspace.models.V1DeviceListItem;

V1DeviceListItem v1DeviceListItem = new V1DeviceListItem.Builder()
    .deviceId("900000000000001")
    .status("LicenseAssignSuccess")
    .reason("Success")
    .build();
```

