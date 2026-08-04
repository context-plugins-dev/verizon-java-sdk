
# Offboarding

## Structure

`Offboarding`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Sensoridentifier` | `String` | Optional | the IEEE EUI64 address space used to identify a device. It is supplied by the device manufacturer | String getSensoridentifier() | setSensoridentifier(String sensoridentifier) |

## Example

```java
import com.verizon.thingspace.models.Offboarding;

Offboarding offboarding = new Offboarding.Builder()
    .sensoridentifier("The unique EUI64 address of the device")
    .build();
```

