
# V2 List of Licenses to Remove Result

List of created license cancellation devices.

## Structure

`V2ListOfLicensesToRemoveResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Count` | `int` | Required | The number of devices. | int getCount() | setCount(int count) |
| `DeviceList` | `List<String>` | Required | Device IMEI list. | List<String> getDeviceList() | setDeviceList(List<String> deviceList) |

## Example

```java
import com.verizon.thingspace.models.V2ListOfLicensesToRemoveResult;
import java.util.Arrays;

V2ListOfLicensesToRemoveResult v2ListOfLicensesToRemoveResult = new V2ListOfLicensesToRemoveResult.Builder(
    2,
    Arrays.asList(
        "990003425730535",
        "990000473475989"
    )
)
.build();
```

