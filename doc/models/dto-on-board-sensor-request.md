
# Dto on Board Sensor Request

## Structure

`DtoOnBoardSensorRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountname` | `String` | Optional | The numeric account name, which must include leading zeros | String getAccountname() | setAccountname(String accountname) |
| `Payload` | [`Payload`](../../doc/models/payload.md) | Optional | - | Payload getPayload() | setPayload(Payload payload) |

## Example

```java
import com.verizon.thingspace.ApiHelper;
import com.verizon.thingspace.models.DtoOnBoardSensorRequest;
import com.verizon.thingspace.models.Payload;
import com.verizon.thingspace.models.ResourceOnBoardSensor;
import java.io.IOException;
import java.util.LinkedHashMap;

DtoOnBoardSensorRequest dtoOnBoardSensorRequest = new DtoOnBoardSensorRequest.Builder()
    .accountname("0000123456-00001")
    .payload(new Payload.Builder()
        .addsensor(new ResourceOnBoardSensor.Builder(
            "deveui6",
            "appeui0",
            "appkey0",
            "class4",
            "kind8",
            "description0",
            "name0"
        )
        .customdata(new LinkedHashMap<String, Object>() {{
                put("key0", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"));
                put("key1", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"));
                put("key2", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"));
            }})
        .build())
        .build())
    .build();
```

