
# Dto Device Action Set Configuration 1

## Structure

`DtoDeviceActionSetConfiguration1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceConfig` | [`DtoDeviceConfig`](../../doc/models/dto-device-config.md) | Optional | - | DtoDeviceConfig getDeviceConfig() | setDeviceConfig(DtoDeviceConfig deviceConfig) |
| `RbsHighPrecisionTiltConfig` | [`RbsHighPrecisionTiltConfig`](../../doc/models/rbs-high-precision-tilt-config.md) | Optional | - | RbsHighPrecisionTiltConfig getRbsHighPrecisionTiltConfig() | setRbsHighPrecisionTiltConfig(RbsHighPrecisionTiltConfig rbsHighPrecisionTiltConfig) |

## Example

```java
import com.verizon.thingspace.models.DtoDeviceActionSetConfiguration1;
import com.verizon.thingspace.models.DtoDeviceConfig;
import com.verizon.thingspace.models.ModeEnum;
import com.verizon.thingspace.models.PeriodicReporting;
import com.verizon.thingspace.models.RbsHighPrecisionTiltConfig;
import com.verizon.thingspace.models.SensorInsightsBLE;
import com.verizon.thingspace.models.UnitEnum;

DtoDeviceActionSetConfiguration1 dtoDeviceActionSetConfiguration1 = new DtoDeviceActionSetConfiguration1.Builder()
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
    .build();
```

