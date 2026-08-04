
# Change PWN Device Profile Request

## Structure

`ChangePWNDeviceProfileRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | - | String getAccountName() | setAccountName(String accountName) |
| `DeviceList` | [`List<PWNDeviceList>`](../../doc/models/pwn-device-list.md) | Required | - | List<PWNDeviceList> getDeviceList() | setDeviceList(List<PWNDeviceList> deviceList) |
| `NewProfile` | `String` | Required | - | String getNewProfile() | setNewProfile(String newProfile) |

## Example

```java
import com.verizon.thingspace.models.ChangePWNDeviceProfileRequest;
import com.verizon.thingspace.models.PWNDeviceId;
import com.verizon.thingspace.models.PWNDeviceList;
import java.util.Arrays;

ChangePWNDeviceProfileRequest changePWNDeviceProfileRequest = new ChangePWNDeviceProfileRequest.Builder(
    "0342351414-00001",
    Arrays.asList(
        new PWNDeviceList.Builder(
            Arrays.asList(
                new PWNDeviceId.Builder(
                    "99948099913024600000",
                    "iccid"
                )
                .build()
            )
        )
        .build()
    ),
    "HSS EsmProfile Enterprise 5G internet"
)
.build();
```

