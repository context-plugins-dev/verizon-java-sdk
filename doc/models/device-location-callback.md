
# Device Location Callback

## Structure

`DeviceLocationCallback`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | [`CallbackServiceNameEnum`](../../doc/models/callback-service-name-enum.md) | Required | The name of the callback service. | CallbackServiceNameEnum getName() | setName(CallbackServiceNameEnum name) |
| `Url` | `String` | Required | The location of your callback listener. | String getUrl() | setUrl(String url) |

## Example

```java
import com.verizon.thingspace.models.CallbackServiceNameEnum;
import com.verizon.thingspace.models.DeviceLocationCallback;

DeviceLocationCallback deviceLocationCallback = new DeviceLocationCallback.Builder(
    CallbackServiceNameEnum.LOCATION,
    "http://10.120.102.183:50559/CallbackListener/LocationServiceMessages.asmx"
)
.build();
```

