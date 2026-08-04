
# Device Upload Request

## Structure

`DeviceUploadRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | - | String getAccountName() | setAccountName(String accountName) |
| `Devices` | [`List<DeviceList>`](../../doc/models/device-list.md) | Required | - | List<DeviceList> getDevices() | setDevices(List<DeviceList> devices) |
| `EmailAddress` | `String` | Required | - | String getEmailAddress() | setEmailAddress(String emailAddress) |
| `DeviceSku` | `String` | Required | - | String getDeviceSku() | setDeviceSku(String deviceSku) |
| `UploadType` | `String` | Required | - | String getUploadType() | setUploadType(String uploadType) |

## Example

```java
import com.verizon.thingspace.models.DeviceId;
import com.verizon.thingspace.models.DeviceList;
import com.verizon.thingspace.models.DeviceUploadRequest;
import java.util.Arrays;

DeviceUploadRequest deviceUploadRequest = new DeviceUploadRequest.Builder(
    "1223334444-00001",
    Arrays.asList(
        new DeviceList.Builder()
            .deviceIds(Arrays.asList(
                new DeviceId.Builder(
                    "id0",
                    "kind8"
                )
                .build()
            ))
            .build()
    ),
    "bob@mycompany.com",
    "VZW123456",
    "IMEI"
)
.build();
```

