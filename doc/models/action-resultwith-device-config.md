
# Action Resultwith Device Config

## Structure

`ActionResultwithDeviceConfig`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Createdon` | `LocalDateTime` | Optional | Timestamp of the record | LocalDateTime getCreatedon() | setCreatedon(LocalDateTime createdon) |
| `Description` | `String` | Optional | - | String getDescription() | setDescription(String description) |
| `Deviceid` | `String` | Optional | This is a UUID value of the device created when the device is onboarded | String getDeviceid() | setDeviceid(String deviceid) |
| `Errmsg` | `String` | Optional | Error message | String getErrmsg() | setErrmsg(String errmsg) |
| `Fields` | [`DtoDeviceActionSetConfiguration`](../../doc/models/dto-device-action-set-configuration.md) | Optional | - | DtoDeviceActionSetConfiguration getFields() | setFields(DtoDeviceActionSetConfiguration fields) |
| `Foreignid` | `String` | Optional | UUID of the ECPD account the user belongs to | String getForeignid() | setForeignid(String foreignid) |
| `Id` | `String` | Optional | UUID of the user record, assigned at creation | String getId() | setId(String id) |
| `Lastupdated` | `LocalDateTime` | Optional | Timestamp of the record | LocalDateTime getLastupdated() | setLastupdated(LocalDateTime lastupdated) |
| `State` | `String` | Optional | The current status of the device or transaction and will be `success` or `failed` | String getState() | setState(String state) |
| `Transactionid` | `String` | Optional | The system-generated UUID of the transaction | String getTransactionid() | setTransactionid(String transactionid) |
| `Version` | `String` | Optional | The resource version | String getVersion() | setVersion(String version) |
| `Versionid` | `String` | Optional | The UUID of the resource version | String getVersionid() | setVersionid(String versionid) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.ActionResultwithDeviceConfig;
import com.verizon.thingspace.models.DtoDeviceActionSetConfiguration;
import com.verizon.thingspace.models.DtoDeviceConfig;
import com.verizon.thingspace.models.SensorInsightsBLE;

ActionResultwithDeviceConfig actionResultwithDeviceConfig = new ActionResultwithDeviceConfig.Builder()
    .createdon(DateTimeHelper.fromRfc8601DateTime("2023-10-02T15:46:34.562Z"))
    .description("description8")
    .deviceid("The UUID of the device")
    .errmsg("provider_service_error")
    .fields(new DtoDeviceActionSetConfiguration.Builder()
        .deviceConfig(new DtoDeviceConfig.Builder()
            .ble(new SensorInsightsBLE.Builder()
                .dataMode(216)
                .manufacturerId(180)
                .maxNumScan(126)
                .minSigStr(60)
                .monitorPeriod(88)
                .build())
            .build())
        .build())
    .foreignid("c1f178d3-eeee-ffff-gggg-0d6b7ae6022a")
    .lastupdated(DateTimeHelper.fromRfc8601DateTime("2023-10-02T15:46:34.562Z"))
    .state("success")
    .transactionid("afbcc00d-eeee-ffff-gggg-38b4333fcf06")
    .version("1.0")
    .versionid("337bd2e8-eeee-ffff-gggg-5207992fd395")
    .build();
```

