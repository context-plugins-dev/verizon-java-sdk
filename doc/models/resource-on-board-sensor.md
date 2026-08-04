
# Resource on Board Sensor

## Structure

`ResourceOnBoardSensor`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Deveui` | `String` | Required | the IEEE EUI64 address space used to identify a device. It is supplied by the device manufacturer | String getDeveui() | setDeveui(String deveui) |
| `Appeui` | `String` | Required | global application ID in IEEE EUI64 address space that uniquely identifies the entity able to process the JoinReq frame | String getAppeui() | setAppeui(String appeui) |
| `Appkey` | `String` | Required | an encryption key used for messages during every over the air activation | String getAppkey() | setAppkey(String appkey) |
| `Class` | `String` | Required | Class of the sensor device. Valid values are Class A (A), Class B (B), and Class C (C). All LoRaWAN devices must implement Class A | String getClassField() | setClassField(String classField) |
| `Kind` | `String` | Required | The kind of sensor device | String getKind() | setKind(String kind) |
| `Description` | `String` | Required | - | String getDescription() | setDescription(String description) |
| `Name` | `String` | Required | - | String getName() | setName(String name) |
| `Customdata` | `Map<String, Object>` | Optional | Name/value pair, where the value is client defined.  The purpose is to keep track of current state per device action. | Map<String, Object> getCustomdata() | setCustomdata(Map<String, Object> customdata) |

## Example

```java
import com.verizon.thingspace.ApiHelper;
import com.verizon.thingspace.models.ResourceOnBoardSensor;
import java.io.IOException;
import java.util.LinkedHashMap;

ResourceOnBoardSensor resourceOnBoardSensor = new ResourceOnBoardSensor.Builder(
    "The unique EUI64 address of the device",
    "application ID",
    "Encryption key",
    "A",
    "ts.device.sensor.lorawan.radiobridge.RBS301-DWS-US",
    "used to identify water leaks",
    "water leak sensor"
)
.customdata(new LinkedHashMap<String, Object>() {{
        put("key0", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"));
        put("key1", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"));
    }})
.build();
```

