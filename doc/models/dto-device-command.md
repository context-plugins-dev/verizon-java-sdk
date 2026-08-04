
# Dto Device Command

## Structure

`DtoDeviceCommand`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Optional | The numeric account name, which must include leading zeros | String getAccountName() | setAccountName(String accountName) |
| `Configuration` | [`Rbstiltconfig`](../../doc/models/rbstiltconfig.md) | Optional | - | Rbstiltconfig getConfiguration() | setConfiguration(Rbstiltconfig configuration) |
| `Resourceidentifier` | [`DtoResourceidentifier`](../../doc/models/dto-resourceidentifier.md) | Optional | - | DtoResourceidentifier getResourceidentifier() | setResourceidentifier(DtoResourceidentifier resourceidentifier) |

## Example

```java
import com.verizon.thingspace.models.DtoDeviceCommand;
import com.verizon.thingspace.models.DtoResourceidentifier;
import com.verizon.thingspace.models.ModeEnum;
import com.verizon.thingspace.models.PeriodicReporting;
import com.verizon.thingspace.models.RbsHighPrecisionTiltConfig;
import com.verizon.thingspace.models.Rbstiltconfig;
import com.verizon.thingspace.models.UnitEnum;

DtoDeviceCommand dtoDeviceCommand = new DtoDeviceCommand.Builder()
    .accountName("0000123456-00001")
    .configuration(new Rbstiltconfig.Builder()
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
    .resourceidentifier(new DtoResourceidentifier.Builder()
        .id("id4")
        .build())
    .build();
```

