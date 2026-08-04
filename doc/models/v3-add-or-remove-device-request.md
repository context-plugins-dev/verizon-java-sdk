
# V3 Add or Remove Device Request

Devices to add or remove from existing software upgrade information.

## Structure

`V3AddOrRemoveDeviceRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | `String` | Required | Operation either 'append' or 'remove' | String getType() | setType(String type) |
| `DeviceList` | `List<String>` | Required | Device IMEI list. | List<String> getDeviceList() | setDeviceList(List<String> deviceList) |

## Example

```java
import com.verizon.thingspace.models.V3AddOrRemoveDeviceRequest;
import java.util.Arrays;

V3AddOrRemoveDeviceRequest v3AddOrRemoveDeviceRequest = new V3AddOrRemoveDeviceRequest.Builder(
    "remove",
    Arrays.asList(
        "15-digit IMEI"
    )
)
.build();
```

