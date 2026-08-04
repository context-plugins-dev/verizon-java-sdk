
# Dm V1 Devices Actions Set Request

## Structure

`DmV1DevicesActionsSetRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountname` | `String` | Optional | The numeric account name, which must include leading zeros | String getAccountname() | setAccountname(String accountname) |
| `Configuration` | [`DtoDeviceActionSetConfiguration1`](../../doc/models/dto-device-action-set-configuration-1.md) | Optional | - | DtoDeviceActionSetConfiguration1 getConfiguration() | setConfiguration(DtoDeviceActionSetConfiguration1 configuration) |
| `Resourceidentifier` | [`DtoDeviceResourceIdentifier1`](../../doc/models/dto-device-resource-identifier-1.md) | Optional | Device identifiers, one or more are required | DtoDeviceResourceIdentifier1 getResourceidentifier() | setResourceidentifier(DtoDeviceResourceIdentifier1 resourceidentifier) |

## Example

```java
import com.verizon.thingspace.models.DmV1DevicesActionsSetRequest;
import com.verizon.thingspace.models.DtoDeviceActionSetConfiguration1;
import com.verizon.thingspace.models.DtoDeviceConfig;
import com.verizon.thingspace.models.DtoDeviceResourceIdentifier1;
import com.verizon.thingspace.models.ModeEnum;
import com.verizon.thingspace.models.PeriodicReporting;
import com.verizon.thingspace.models.RbsHighPrecisionTiltConfig;
import com.verizon.thingspace.models.SensorInsightsBLE;
import com.verizon.thingspace.models.UnitEnum;

DmV1DevicesActionsSetRequest dmV1DevicesActionsSetRequest = new DmV1DevicesActionsSetRequest.Builder()
    .accountname("0000123456-00001")
    .configuration(new DtoDeviceActionSetConfiguration1.Builder()
        .deviceConfig(new DtoDeviceConfig.Builder()
            .ble(new SensorInsightsBLE.Builder()
                .dataMode(216)
                .manufacturerId(180)
                .maxNumScan(126)
                .minSigStr(60)
                .monitorPeriod(88)
                .build())
            .build())
        .rbsHighPrecisionTiltConfig(new RbsHighPrecisionTiltConfig.Builder()
            .mode(ModeEnum.REPORTONCHANGE)
            .periodicReporting(new PeriodicReporting.Builder()
                .unit(UnitEnum.MINUTES)
                .hours(250)
                .minutes(232)
                .build())
            .holdTime(62)
            .angleAway(90)
            .angleToward(30)
            .build())
        .build())
    .resourceidentifier(new DtoDeviceResourceIdentifier1.Builder()
        .deveui("deveui2")
        .deviceid("deviceid6")
        .esn(86)
        .iccid("iccid0")
        .imei(2)
        .build())
    .build();
```

