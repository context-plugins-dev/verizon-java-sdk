
# Rbstiltconfig

## Structure

`Rbstiltconfig`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `RbsHighPrecisionTiltConfig` | [`RbsHighPrecisionTiltConfig`](../../doc/models/rbs-high-precision-tilt-config.md) | Optional | - | RbsHighPrecisionTiltConfig getRbsHighPrecisionTiltConfig() | setRbsHighPrecisionTiltConfig(RbsHighPrecisionTiltConfig rbsHighPrecisionTiltConfig) |

## Example

```java
import com.verizon.thingspace.models.ModeEnum;
import com.verizon.thingspace.models.PeriodicReporting;
import com.verizon.thingspace.models.RbsHighPrecisionTiltConfig;
import com.verizon.thingspace.models.Rbstiltconfig;
import com.verizon.thingspace.models.UnitEnum;

Rbstiltconfig rbstiltconfig = new Rbstiltconfig.Builder()
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

