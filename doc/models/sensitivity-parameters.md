
# Sensitivity Parameters

Details for sensitivity parameters.

## Structure

`SensitivityParameters`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AbnormalMaxValue` | `Double` | Optional | The maximum value of the threshold in the units being measured. | Double getAbnormalMaxValue() | setAbnormalMaxValue(Double abnormalMaxValue) |
| `EnableAbnormal` | `Boolean` | Optional | If abnormal values are being monitored.<br />true - Monitor for abnormal values<br />false - Do not monitor for abnormal values. | Boolean getEnableAbnormal() | setEnableAbnormal(Boolean enableAbnormal) |
| `EnableVeryAbnormal` | `Boolean` | Optional | If very abnormal values are being monitored.<br />true - Monitor for very abnormal values<br />false - Do not monitor for very abnormal values. | Boolean getEnableVeryAbnormal() | setEnableVeryAbnormal(Boolean enableVeryAbnormal) |
| `VeryAbnormalMaxValue` | `Double` | Optional | The maximum value of the threshold in the units being measured. | Double getVeryAbnormalMaxValue() | setVeryAbnormalMaxValue(Double veryAbnormalMaxValue) |

## Example

```java
import com.verizon.thingspace.models.SensitivityParameters;

SensitivityParameters sensitivityParameters = new SensitivityParameters.Builder()
    .abnormalMaxValue(1.1D)
    .enableAbnormal(true)
    .enableVeryAbnormal(true)
    .veryAbnormalMaxValue(0.55D)
    .build();
```

