
# V1 Licenses Assigned Removed Result

License assignment or removal confirmation.

## Structure

`V1LicensesAssignedRemovedResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Optional | Account identifier in "##########-#####". | String getAccountName() | setAccountName(String accountName) |
| `LicCount` | `Integer` | Optional | Total number of monthly licenses in an MRC subscription. | Integer getLicCount() | setLicCount(Integer licCount) |
| `LicUsedCount` | `Integer` | Optional | Number of licenses assigned to devices after the request completed. | Integer getLicUsedCount() | setLicUsedCount(Integer licUsedCount) |
| `DeviceList` | [`List<V1DeviceListItem>`](../../doc/models/v1-device-list-item.md) | Optional | A JSON object for each device that was in the request. | List<V1DeviceListItem> getDeviceList() | setDeviceList(List<V1DeviceListItem> deviceList) |

## Example

```java
import com.verizon.thingspace.models.V1DeviceListItem;
import com.verizon.thingspace.models.V1LicensesAssignedRemovedResult;
import java.util.Arrays;

V1LicensesAssignedRemovedResult v1LicensesAssignedRemovedResult = new V1LicensesAssignedRemovedResult.Builder()
    .accountName("0242078689-00001")
    .licCount(9000)
    .licUsedCount(1000)
    .deviceList(Arrays.asList(
        new V1DeviceListItem.Builder()
            .deviceId("900000000000001")
            .status("LicenseAssignSuccess")
            .reason("Success")
            .build(),
        new V1DeviceListItem.Builder()
            .deviceId("900000000000999")
            .status("LicenseAssignSuccess")
            .reason("Success")
            .build()
    ))
    .build();
```

