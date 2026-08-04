
# Profile Change State Request

## Structure

`ProfileChangeStateRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Devices` | [`List<DeviceList>`](../../doc/models/device-list.md) | Required | - | List<DeviceList> getDevices() | setDevices(List<DeviceList> devices) |
| `AccountName` | `String` | Required | - | String getAccountName() | setAccountName(String accountName) |
| `SmsrOid` | `String` | Required | - | String getSmsrOid() | setSmsrOid(String smsrOid) |

## Example

```java
import com.verizon.thingspace.models.DeviceId;
import com.verizon.thingspace.models.DeviceList;
import com.verizon.thingspace.models.ProfileChangeStateRequest;
import java.util.Arrays;

ProfileChangeStateRequest profileChangeStateRequest = new ProfileChangeStateRequest.Builder(
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
    "1223334444-00001",
    "1.3.6.1.4.1.31746.1.500.200.101.5"
)
.build();
```

