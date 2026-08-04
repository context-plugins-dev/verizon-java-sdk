
# Dto Sensor on Board Status Request

## Structure

`DtoSensorOnBoardStatusRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountname` | `String` | Optional | The numeric account name, which must include leading zeros | String getAccountname() | setAccountname(String accountname) |
| `Gatewayidentifier` | [`Gatewayidentifier`](../../doc/models/gatewayidentifier.md) | Optional | - | Gatewayidentifier getGatewayidentifier() | setGatewayidentifier(Gatewayidentifier gatewayidentifier) |
| `Onboarding` | [`Onboarding`](../../doc/models/onboarding.md) | Optional | - | Onboarding getOnboarding() | setOnboarding(Onboarding onboarding) |

## Example

```java
import com.verizon.thingspace.models.DtoSensorOnBoardStatusRequest;
import com.verizon.thingspace.models.Gatewayidentifier;
import com.verizon.thingspace.models.Onboarding;

DtoSensorOnBoardStatusRequest dtoSensorOnBoardStatusRequest = new DtoSensorOnBoardStatusRequest.Builder()
    .accountname("0000123456-00001")
    .gatewayidentifier(new Gatewayidentifier.Builder()
        .deviceid("deviceid0")
        .build())
    .onboarding(new Onboarding.Builder()
        .sensoridentifier("sensoridentifier4")
        .build())
    .build();
```

