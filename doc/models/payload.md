
# Payload

## Structure

`Payload`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Addsensor` | [`ResourceOnBoardSensor`](../../doc/models/resource-on-board-sensor.md) | Optional | - | ResourceOnBoardSensor getAddsensor() | setAddsensor(ResourceOnBoardSensor addsensor) |

## Example

```java
import com.verizon.thingspace.ApiHelper;
import com.verizon.thingspace.models.Payload;
import com.verizon.thingspace.models.ResourceOnBoardSensor;
import java.io.IOException;
import java.util.LinkedHashMap;

Payload payload = new Payload.Builder()
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
    .build();
```

