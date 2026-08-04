
# Firmware Upgrade Request

Details of the firmware upgrade request.

## Structure

`FirmwareUpgradeRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | Account identifier in "##########-#####". | String getAccountName() | setAccountName(String accountName) |
| `FirmwareName` | `String` | Required | The name of the firmware image that will be used for the upgrade, from a GET /firmware response. | String getFirmwareName() | setFirmwareName(String firmwareName) |
| `FirmwareTo` | `String` | Required | The name of the firmware version that will be on the devices after a successful upgrade. | String getFirmwareTo() | setFirmwareTo(String firmwareTo) |
| `StartDate` | `LocalDate` | Required | The date that the upgrade begins. | LocalDate getStartDate() | setStartDate(LocalDate startDate) |
| `EndDate` | `LocalDate` | Required | The date that the upgrade ends. | LocalDate getEndDate() | setEndDate(LocalDate endDate) |
| `DeviceList` | `List<String>` | Required | The IMEIs of the devices. | List<String> getDeviceList() | setDeviceList(List<String> deviceList) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.FirmwareUpgradeRequest;
import java.util.Arrays;

FirmwareUpgradeRequest firmwareUpgradeRequest = new FirmwareUpgradeRequest.Builder(
    "0402196254-00001",
    "FOTA_Verizon_Model-A_01To02_HF",
    "VerizonFirmwareVersion-02",
    DateTimeHelper.fromSimpleDate("2018-04-01"),
    DateTimeHelper.fromSimpleDate("2018-04-05"),
    Arrays.asList(
        "990003425730535",
        "990000473475989",
        "990005733420535",
        "990000347475989",
        "990007303425535",
        "990007590473489"
    )
)
.build();
```

