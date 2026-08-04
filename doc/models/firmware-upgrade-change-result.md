
# Firmware Upgrade Change Result

Upgrade information.

## Structure

`FirmwareUpgradeChangeResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Optional | Account identifier in "##########-#####". | String getAccountName() | setAccountName(String accountName) |
| `Id` | `String` | Optional | The unique identifier for this upgrade. | String getId() | setId(String id) |
| `DeviceList` | [`List<V1DeviceListItem>`](../../doc/models/v1-device-list-item.md) | Optional | A JSON object for each device that was included in the request, showing the device IMEI, the status of the addition or removal, and additional information about the status. | List<V1DeviceListItem> getDeviceList() | setDeviceList(List<V1DeviceListItem> deviceList) |

## Example

```java
import com.verizon.thingspace.models.FirmwareUpgradeChangeResult;
import com.verizon.thingspace.models.V1DeviceListItem;
import java.util.Arrays;

FirmwareUpgradeChangeResult firmwareUpgradeChangeResult = new FirmwareUpgradeChangeResult.Builder()
    .accountName("0000123456-00001")
    .id("60b5d639-ccdc-4db8-8824-069bd94c95bf")
    .deviceList(Arrays.asList(
        new V1DeviceListItem.Builder()
            .deviceId("15-digit IMEI")
            .status("AddDeviceSucceed")
            .reason("Device added Successfully")
            .build(),
        new V1DeviceListItem.Builder()
            .deviceId("15-digit IMEI")
            .status("AddDeviceSucceed")
            .reason("Device added Successfully")
            .build()
    ))
    .build();
```

