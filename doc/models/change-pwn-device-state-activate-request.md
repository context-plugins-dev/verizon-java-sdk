
# Change PWN Device State Activate Request

## Structure

`ChangePWNDeviceStateActivateRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | - | String getAccountName() | setAccountName(String accountName) |
| `DeviceList` | [`List<PWNDeviceList>`](../../doc/models/pwn-device-list.md) | Required | - | List<PWNDeviceList> getDeviceList() | setDeviceList(List<PWNDeviceList> deviceList) |
| `Activate` | [`Activate`](../../doc/models/activate.md) | Required | - | Activate getActivate() | setActivate(Activate activate) |

## Example

```java
import com.verizon.thingspace.models.Activate;
import com.verizon.thingspace.models.ChangePWNDeviceStateActivateRequest;
import com.verizon.thingspace.models.PWNDeviceId;
import com.verizon.thingspace.models.PWNDeviceList;
import java.util.Arrays;

ChangePWNDeviceStateActivateRequest changePWNDeviceStateActivateRequest = new ChangePWNDeviceStateActivateRequest.Builder(
    "0342351414-00001",
    Arrays.asList(
        new PWNDeviceList.Builder(
            Arrays.asList(
                new PWNDeviceId.Builder(
                    "99948099913024600001",
                    "iccid"
                )
                .build()
            )
        )
        .build()
    ),
    new Activate.Builder(
        "HSS EsmProfile Enterprise 5G"
    )
    .build()
)
.build();
```

