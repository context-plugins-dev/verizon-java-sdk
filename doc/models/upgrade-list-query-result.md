
# Upgrade List Query Result

Upgrade information.

## Structure

`UpgradeListQueryResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `HasMoreFlag` | `Boolean` | Optional | True if there are more devices to retrieve. | Boolean getHasMoreFlag() | setHasMoreFlag(Boolean hasMoreFlag) |
| `LastSeenUpgradeId` | `Integer` | Optional | If hasMoreData=true, the startIndex to use for the next request. 0 if hasMoreData=false. | Integer getLastSeenUpgradeId() | setLastSeenUpgradeId(Integer lastSeenUpgradeId) |
| `ReportList` | [`List<FirmwareUpgrade>`](../../doc/models/firmware-upgrade.md) | Optional | Array of upgrade objects with the specified status. | List<FirmwareUpgrade> getReportList() | setReportList(List<FirmwareUpgrade> reportList) |

## Example

```java
import com.verizon.thingspace.models.FirmwareUpgrade;
import com.verizon.thingspace.models.FirmwareUpgradeDeviceListItem;
import com.verizon.thingspace.models.UpgradeListQueryResult;
import java.util.Arrays;

UpgradeListQueryResult upgradeListQueryResult = new UpgradeListQueryResult.Builder()
    .hasMoreFlag(false)
    .lastSeenUpgradeId(116)
    .reportList(Arrays.asList(
        new FirmwareUpgrade.Builder()
            .id("3ac8c863-bde7-4f41-878e-dd5473e973bb")
            .accountName("0242078689-00001")
            .firmwareName("FOTA_Verizon_Model-A_01To02_HF")
            .firmwareTo("VerizonFirmwareVersion-02")
            .startDate("2018-04-01")
            .status("Queued")
            .deviceList(Arrays.asList(
                new FirmwareUpgradeDeviceListItem.Builder()
                    .deviceId("900000000000002")
                    .status("Device Accepted")
                    .resultReason("success")
                    .build(),
                new FirmwareUpgradeDeviceListItem.Builder()
                    .deviceId("900000000000003")
                    .status("Device Accepted")
                    .resultReason("success")
                    .build()
            ))
            .build(),
        new FirmwareUpgrade.Builder()
            .id("efb8206b-2e88-4fdb-886d-31d8e87cd95f")
            .accountName("0242078689-00001")
            .firmwareName("FOTA_Verizon_Model-A_01To02_HF")
            .firmwareTo("VerizonFirmwareVersion-02")
            .startDate("2018-04-01T16:03:00.000Z")
            .status("Queued")
            .deviceList(Arrays.asList(
                new FirmwareUpgradeDeviceListItem.Builder()
                    .deviceId("900000000000008")
                    .status("Device Accepted")
                    .resultReason("success")
                    .build()
            ))
            .build()
    ))
    .build();
```

