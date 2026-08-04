
# M5 G Bi Request Response

## Structure

`M5gBiRequestResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `RequestId` | `String` | Optional | - | String getRequestId() | setRequestId(String requestId) |

## Example

```java
import com.verizon.thingspace.models.M5gBiRequestResponse;

M5gBiRequestResponse m5gBiRequestResponse = new M5gBiRequestResponse.Builder()
    .requestId("d1f08526-5443-4054-9a29-4456490ea9f8")
    .build();
```

