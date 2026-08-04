
# V3 Account Device

Device information.

## Structure

`V3AccountDevice`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceId` | `String` | Required | Device identifier. | String getDeviceId() | setDeviceId(String deviceId) |
| `Mdn` | `String` | Required | MDN. | String getMdn() | setMdn(String mdn) |
| `Model` | `String` | Required | Device model. | String getModel() | setModel(String model) |
| `Make` | `String` | Required | Device make. | String getMake() | setMake(String make) |
| `Firmware` | `String` | Required | Device firmware version. | String getFirmware() | setFirmware(String firmware) |
| `FotaEligible` | `boolean` | Required | Value=true if the device software can be upgraded over the air using the Software Management Services API. | boolean getFotaEligible() | setFotaEligible(boolean fotaEligible) |
| `Status` | `String` | Required | Device status. | String getStatus() | setStatus(String status) |
| `LicenseAssigned` | `boolean` | Required | License assigned device. | boolean getLicenseAssigned() | setLicenseAssigned(boolean licenseAssigned) |
| `Protocol` | `String` | Required | Firmware protocol. Valid values include: LWM2M, OMADM, HTTP or NONE. | String getProtocol() | setProtocol(String protocol) |
| `SoftwareList` | [`List<V3SoftwareInfo>`](../../doc/models/v3-software-info.md) | Required | List of sofware. | List<V3SoftwareInfo> getSoftwareList() | setSoftwareList(List<V3SoftwareInfo> softwareList) |
| `FileList` | [`List<V3SoftwareInfo>`](../../doc/models/v3-software-info.md) | Optional | List of files. | List<V3SoftwareInfo> getFileList() | setFileList(List<V3SoftwareInfo> fileList) |
| `CreateTime` | `String` | Optional | The date and time of when the device is created. | String getCreateTime() | setCreateTime(String createTime) |
| `UpgradeTime` | `String` | Optional | The date and time of when the device firmware or software is updated. | String getUpgradeTime() | setUpgradeTime(String upgradeTime) |
| `UpdateTime` | `String` | Optional | The date and time of when the device is updated. | String getUpdateTime() | setUpdateTime(String updateTime) |
| `RefreshTime` | `String` | Optional | The date and time of when the device is refreshed. | String getRefreshTime() | setRefreshTime(String refreshTime) |

## Example

```java
import com.verizon.thingspace.models.V3AccountDevice;
import com.verizon.thingspace.models.V3SoftwareInfo;
import java.util.Arrays;

V3AccountDevice v3AccountDevice = new V3AccountDevice.Builder(
    "15-digit device ID",
    "10-digit MDN",
    "BG96",
    "QUECTEL",
    "BG96MAR04A04M1G",
    false,
    "Active",
    true,
    "LWM2M",
    Arrays.asList(
        new V3SoftwareInfo.Builder(
            "VZ_MDM_IOT",
            "0.14",
            "2012-04-23T18:25:43.511Z"
        )
        .build()
    )
)
.fileList(Arrays.asList(
        new V3SoftwareInfo.Builder(
            "VZ_MDM_IOT",
            "0.14",
            "2012-04-23T18:25:43.511Z"
        )
        .build()
    ))
.createTime("2021-06-03 00:03:56.079 +0000 UTC")
.upgradeTime("2021-06-03 00:03:56.079 +0000 UTC")
.updateTime("2021-06-03 00:03:56.079 +0000 UTC")
.refreshTime("2021-06-03 00:03:56.079 +0000 UTC")
.build();
```

