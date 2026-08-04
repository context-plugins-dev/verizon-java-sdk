
# Device Provisioning History List Request

Request to return the provisioning history of a specified device during a specified time period.

## Structure

`DeviceProvisioningHistoryListRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceId` | [`DeviceId`](../../doc/models/device-id.md) | Required | An identifier for a single device. | DeviceId getDeviceId() | setDeviceId(DeviceId deviceId) |
| `Earliest` | `String` | Required | The earliest date and time for which you want provisioning data. | String getEarliest() | setEarliest(String earliest) |
| `Latest` | `String` | Required | The last date and time for which you want provisioning data. | String getLatest() | setLatest(String latest) |

## Example

```java
import com.verizon.thingspace.models.DeviceId;
import com.verizon.thingspace.models.DeviceProvisioningHistoryListRequest;

DeviceProvisioningHistoryListRequest deviceProvisioningHistoryListRequest = new DeviceProvisioningHistoryListRequest.Builder(
    new DeviceId.Builder(
        "89141390780800784259",
        "iccid"
    )
    .build(),
    "2015-09-16T00:00:01Z",
    "2015-09-18T00:00:01Z"
)
.build();
```

