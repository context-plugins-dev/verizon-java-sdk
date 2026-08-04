
# PWN Device List

## Structure

`PWNDeviceList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceIds` | [`List<PWNDeviceId>`](../../doc/models/pwn-device-id.md) | Required | - | List<PWNDeviceId> getDeviceIds() | setDeviceIds(List<PWNDeviceId> deviceIds) |

## Example

```java
import com.verizon.thingspace.models.PWNDeviceId;
import com.verizon.thingspace.models.PWNDeviceList;
import java.util.Arrays;

PWNDeviceList pWNDeviceList = new PWNDeviceList.Builder(
    Arrays.asList(
        new PWNDeviceId.Builder(
            "99948099913024600001",
            "iccid"
        )
        .build()
    )
)
.build();
```

