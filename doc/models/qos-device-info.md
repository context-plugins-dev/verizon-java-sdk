
# Qos Device Info

## Structure

`QosDeviceInfo`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceId` | [`QosDeviceId`](../../doc/models/qos-device-id.md) | Required | - | QosDeviceId getDeviceId() | setDeviceId(QosDeviceId deviceId) |
| `DeviceIPv6Addr` | `String` | Optional | - | String getDeviceIPv6Addr() | setDeviceIPv6Addr(String deviceIPv6Addr) |
| `FlowInfo` | [`List<FlowInfo>`](../../doc/models/flow-info.md) | Required | - | List<FlowInfo> getFlowInfo() | setFlowInfo(List<FlowInfo> flowInfo) |

## Example

```java
import com.verizon.thingspace.models.FlowInfo;
import com.verizon.thingspace.models.QosDeviceId;
import com.verizon.thingspace.models.QosDeviceInfo;
import java.util.Arrays;

QosDeviceInfo qosDeviceInfo = new QosDeviceInfo.Builder(
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
.build();
```

