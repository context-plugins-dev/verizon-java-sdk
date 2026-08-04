
# V2 List of Licenses to Remove Request

License cancellation candidate devices.

## Structure

`V2ListOfLicensesToRemoveRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | `String` | Optional | List creation option. | String getType() | setType(String type) |
| `Count` | `Integer` | Optional | The number of devices. | Integer getCount() | setCount(Integer count) |
| `DeviceList` | `List<String>` | Required | Device IMEI list. | List<String> getDeviceList() | setDeviceList(List<String> deviceList) |

## Example

```java
import com.verizon.thingspace.models.V2ListOfLicensesToRemoveRequest;
import java.util.Arrays;

V2ListOfLicensesToRemoveRequest v2ListOfLicensesToRemoveRequest = new V2ListOfLicensesToRemoveRequest.Builder(
    Arrays.asList(
        "990003425730535",
        "990000473475989"
    )
)
.type("append")
.count(2)
.build();
```

