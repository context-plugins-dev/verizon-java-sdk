
# Dto Sensor Off Board Status Request

## Structure

`DtoSensorOffBoardStatusRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountname` | `String` | Optional | The numeric account name, which must include leading zeros | String getAccountname() | setAccountname(String accountname) |
| `Gatewayidentifier` | [`Gatewayidentifier`](../../doc/models/gatewayidentifier.md) | Optional | - | Gatewayidentifier getGatewayidentifier() | setGatewayidentifier(Gatewayidentifier gatewayidentifier) |
| `Offboarding` | [`Offboarding`](../../doc/models/offboarding.md) | Optional | - | Offboarding getOffboarding() | setOffboarding(Offboarding offboarding) |

## Example

```java
import com.verizon.thingspace.models.DtoSensorOffBoardStatusRequest;
import com.verizon.thingspace.models.Gatewayidentifier;
import com.verizon.thingspace.models.Offboarding;

DtoSensorOffBoardStatusRequest dtoSensorOffBoardStatusRequest = new DtoSensorOffBoardStatusRequest.Builder()
    .accountname("0000123456-00001")
    .gatewayidentifier(new Gatewayidentifier.Builder()
        .deviceid("deviceid0")
        .build())
    .offboarding(new Offboarding.Builder()
        .sensoridentifier("sensoridentifier8")
        .build())
    .build();
```

