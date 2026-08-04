
# V1 List of Licenses to Remove Result

List of licenses assigned.

## Structure

`V1ListOfLicensesToRemoveResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Count` | `Integer` | Optional | The total number of devices on the cancellation candidate list. | Integer getCount() | setCount(Integer count) |
| `DeviceList` | `List<String>` | Optional | The IMEIs of the devices. | List<String> getDeviceList() | setDeviceList(List<String> deviceList) |

## Example

```java
import com.verizon.thingspace.models.V1ListOfLicensesToRemoveResult;
import java.util.Arrays;

V1ListOfLicensesToRemoveResult v1ListOfLicensesToRemoveResult = new V1ListOfLicensesToRemoveResult.Builder()
    .count(2)
    .deviceList(Arrays.asList(
        "900000000000001",
        "900000000000999"
    ))
    .build();
```

