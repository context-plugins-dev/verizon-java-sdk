
# V3 Device List Item

Device changed.

## Structure

`V3DeviceListItem`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceId` | `String` | Optional | Device IMEI. | String getDeviceId() | setDeviceId(String deviceId) |
| `Status` | `String` | Optional | Success or failure. | String getStatus() | setStatus(String status) |
| `Reason` | `String` | Optional | Result reason. | String getReason() | setReason(String reason) |

## Example

```java
import com.verizon.thingspace.models.V3DeviceListItem;

V3DeviceListItem v3DeviceListItem = new V3DeviceListItem.Builder()
    .deviceId("15-digit IMEI")
    .status("AddDeviceSucceed")
    .reason("Device added Successfully")
    .build();
```

