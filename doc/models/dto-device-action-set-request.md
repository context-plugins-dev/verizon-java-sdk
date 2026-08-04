
# Dto Device Action Set Request

## Structure

`DtoDeviceActionSetRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountname` | `String` | Optional | The numeric account name, which must include leading zeros | String getAccountname() | setAccountname(String accountname) |
| `Configuration` | [`DtoDeviceActionSetConfiguration`](../../doc/models/dto-device-action-set-configuration.md) | Optional | - | DtoDeviceActionSetConfiguration getConfiguration() | setConfiguration(DtoDeviceActionSetConfiguration configuration) |
| `Resourceidentifier` | [`DtoDeviceResourceIdentifier`](../../doc/models/dto-device-resource-identifier.md) | Optional | Device identifiers, one or more are required | DtoDeviceResourceIdentifier getResourceidentifier() | setResourceidentifier(DtoDeviceResourceIdentifier resourceidentifier) |

## Example

```java
import com.verizon.thingspace.models.DtoDeviceActionSetConfiguration;
import com.verizon.thingspace.models.DtoDeviceActionSetRequest;
import com.verizon.thingspace.models.DtoDeviceConfig;
import com.verizon.thingspace.models.DtoDeviceResourceIdentifier;
import com.verizon.thingspace.models.SensorInsightsBLE;

DtoDeviceActionSetRequest dtoDeviceActionSetRequest = new DtoDeviceActionSetRequest.Builder()
    .accountname("0000123456-00001")
    .configuration(new DtoDeviceActionSetConfiguration.Builder()
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
    .resourceidentifier(new DtoDeviceResourceIdentifier.Builder()
        .deveui("deveui2")
        .deviceid("deviceid6")
        .esn(86)
        .iccid("iccid0")
        .imei(2)
        .build())
    .build();
```

