
# Get Device Experience Score History Request

Get device experience score history.

## Structure

`GetDeviceExperienceScoreHistoryRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | Account name.<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `32`, *Pattern*: `^[0-9-]{3,32}$` | String getAccountName() | setAccountName(String accountName) |
| `DeviceId` | [`DeviceIdentifier`](../../doc/models/device-identifier.md) | Required | Device Id details. | DeviceIdentifier getDeviceId() | setDeviceId(DeviceIdentifier deviceId) |

## Example

```java
import com.verizon.thingspace.models.DeviceIdentifier;
import com.verizon.thingspace.models.GetDeviceExperienceScoreHistoryRequest;

GetDeviceExperienceScoreHistoryRequest getDeviceExperienceScoreHistoryRequest = new GetDeviceExperienceScoreHistoryRequest.Builder(
    "0000123456-00001",
    new DeviceIdentifier.Builder(
        "iccid",
        "01234567899876543210"
    )
    .mdn("0123456789")
    .build()
)
.build();
```

