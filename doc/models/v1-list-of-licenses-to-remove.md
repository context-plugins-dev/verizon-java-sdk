
# V1 List of Licenses to Remove

List of cancellation candidate devices.

## Structure

`V1ListOfLicensesToRemove`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Count` | `Integer` | Optional | The total number of devices on the list. | Integer getCount() | setCount(Integer count) |
| `HasMoreData` | `Boolean` | Optional | True if there are more devices to retrieve. | Boolean getHasMoreData() | setHasMoreData(Boolean hasMoreData) |
| `UpdateTime` | `LocalDateTime` | Optional | The date and time that the list was last updated. | LocalDateTime getUpdateTime() | setUpdateTime(LocalDateTime updateTime) |
| `DeviceList` | `List<String>` | Optional | The IMEIs of the devices. | List<String> getDeviceList() | setDeviceList(List<String> deviceList) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.V1ListOfLicensesToRemove;
import java.util.Arrays;

V1ListOfLicensesToRemove v1ListOfLicensesToRemove = new V1ListOfLicensesToRemove.Builder()
    .count(6)
    .hasMoreData(false)
    .updateTime(DateTimeHelper.fromRfc8601DateTime("2018-03-22T12:06:06.000Z"))
    .deviceList(Arrays.asList(
        "990003425730535",
        "990000473475989",
        "990005733420535",
        "990000347475989",
        "990007303425535",
        "990007590473489"
    ))
    .build();
```

