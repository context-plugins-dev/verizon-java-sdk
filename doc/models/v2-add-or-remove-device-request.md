
# V2 Add or Remove Device Request

Add or remove device to existing software upgrade information.

## Structure

`V2AddOrRemoveDeviceRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | `String` | Required | Operation either 'append' or 'remove'. | String getType() | setType(String type) |
| `DeviceList` | `List<String>` | Required | Device IMEI list. | List<String> getDeviceList() | setDeviceList(List<String> deviceList) |

## Example

```java
import com.verizon.thingspace.models.V2AddOrRemoveDeviceRequest;
import java.util.Arrays;

V2AddOrRemoveDeviceRequest v2AddOrRemoveDeviceRequest = new V2AddOrRemoveDeviceRequest.Builder(
    "remove",
    Arrays.asList(
        "990013907884259",
        "990013907835573",
        "990013907833575"
    )
)
.build();
```

