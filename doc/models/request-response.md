
# Request Response

## Structure

`RequestResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `RequestId` | `String` | Optional | - | String getRequestId() | setRequestId(String requestId) |

## Example

```java
import com.verizon.thingspace.models.RequestResponse;

RequestResponse requestResponse = new RequestResponse.Builder()
    .requestId("595f5c44-eeee-ffff-gggg-020a1545a84d")
    .build();
```

