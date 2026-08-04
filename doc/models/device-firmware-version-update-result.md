
# Device Firmware Version Update Result

Device firmware version update response.

## Structure

`DeviceFirmwareVersionUpdateResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | Account identifier. | String getAccountName() | setAccountName(String accountName) |
| `RequestId` | `String` | Required | Request identifier. | String getRequestId() | setRequestId(String requestId) |

## Example

```java
import com.verizon.thingspace.models.DeviceFirmwareVersionUpdateResult;

DeviceFirmwareVersionUpdateResult deviceFirmwareVersionUpdateResult = new DeviceFirmwareVersionUpdateResult.Builder(
    "accountName8",
    "requestId6"
)
.build();
```

