
# Get Device Experience Score Bulk Request

Get device experience score bulk request.

## Structure

`GetDeviceExperienceScoreBulkRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | Account name.<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `32`, *Pattern*: `^[0-9-]{3,32}$` | String getAccountName() | setAccountName(String accountName) |
| `DeviceList` | [`List<DeviceIdentifier>`](../../doc/models/device-identifier.md) | Required | **Constraints**: *Maximum Items*: `100` | List<DeviceIdentifier> getDeviceList() | setDeviceList(List<DeviceIdentifier> deviceList) |

## Example

```java
import com.verizon.thingspace.models.DeviceIdentifier;
import com.verizon.thingspace.models.GetDeviceExperienceScoreBulkRequest;
import java.util.Arrays;

GetDeviceExperienceScoreBulkRequest getDeviceExperienceScoreBulkRequest = new GetDeviceExperienceScoreBulkRequest.Builder(
    "0000123456-00001",
    Arrays.asList(
        new DeviceIdentifier.Builder(
            "iccid",
            "01234567899876543210"
        )
        .mdn("0123456789")
        .build()
    )
)
.build();
```

