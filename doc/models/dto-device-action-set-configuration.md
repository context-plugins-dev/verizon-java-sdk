
# Dto Device Action Set Configuration

## Structure

`DtoDeviceActionSetConfiguration`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceConfig` | [`DtoDeviceConfig`](../../doc/models/dto-device-config.md) | Optional | - | DtoDeviceConfig getDeviceConfig() | setDeviceConfig(DtoDeviceConfig deviceConfig) |

## Example

```java
import com.verizon.thingspace.models.DtoDeviceActionSetConfiguration;
import com.verizon.thingspace.models.DtoDeviceConfig;
import com.verizon.thingspace.models.SensorInsightsBLE;

DtoDeviceActionSetConfiguration dtoDeviceActionSetConfiguration = new DtoDeviceActionSetConfiguration.Builder()
    .deviceConfig(new DtoDeviceConfig.Builder()
        .ble(new SensorInsightsBLE.Builder()
            .dataMode(216)
            .manufacturerId(180)
            .maxNumScan(126)
            .minSigStr(60)
            .monitorPeriod(88)
            .build())
        .build())
    .build();
```

