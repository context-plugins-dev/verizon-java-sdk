
# Software Package

Software package information.

## Structure

`SoftwarePackage`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SoftwareName` | `String` | Required | Software name. | String getSoftwareName() | setSoftwareName(String softwareName) |
| `LaunchDate` | `LocalDate` | Required | Software launch date. | LocalDate getLaunchDate() | setLaunchDate(LocalDate launchDate) |
| `ReleaseNote` | `String` | Optional | Software release note reserved for future use. | String getReleaseNote() | setReleaseNote(String releaseNote) |
| `Model` | `String` | Required | Software applicable device model. | String getModel() | setModel(String model) |
| `Make` | `String` | Required | Software applicable device make. | String getMake() | setMake(String make) |
| `DistributionType` | `String` | Required | LWM2M, OMD-DM or HTTP. | String getDistributionType() | setDistributionType(String distributionType) |
| `DevicePlatformId` | `String` | Required | The platform (Android, iOS, etc.) that the software can be applied to. | String getDevicePlatformId() | setDevicePlatformId(String devicePlatformId) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.SoftwarePackage;

SoftwarePackage softwarePackage = new SoftwarePackage.Builder(
    "FOTA_Verizon_Model-A_02To03_HF",
    DateTimeHelper.fromSimpleDate("2020-08-31"),
    "Model-A",
    "Verizon",
    "HTTP",
    "IoT"
)
.releaseNote("")
.build();
```

