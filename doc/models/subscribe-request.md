
# Subscribe Request

## Structure

`SubscribeRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | - | String getAccountName() | setAccountName(String accountName) |
| `DeviceInfo` | [`List<QosDeviceInfo>`](../../doc/models/qos-device-info.md) | Required | - | List<QosDeviceInfo> getDeviceInfo() | setDeviceInfo(List<QosDeviceInfo> deviceInfo) |

## Example

```java
import com.verizon.thingspace.models.FlowInfo;
import com.verizon.thingspace.models.QosDeviceId;
import com.verizon.thingspace.models.QosDeviceInfo;
import com.verizon.thingspace.models.SubscribeRequest;
import java.util.Arrays;

SubscribeRequest subscribeRequest = new SubscribeRequest.Builder(
    "0000123456-00001",
    Arrays.asList(
        new QosDeviceInfo.Builder(
            new QosDeviceId.Builder()
                .id("10-digit phone number")
                .kind("mdn")
                .build(),
            Arrays.asList(
                new FlowInfo.Builder()
                    .flowServer("[IPv6 address]:port")
                    .flowDevice("[IPv6 address]:port")
                    .flowDirection("UPLINK")
                    .flowProtocol("UDP")
                    .qciOption("Premium")
                    .build()
            )
        )
        .deviceIPv6Addr("IPv6 address")
        .build()
    )
)
.build();
```

