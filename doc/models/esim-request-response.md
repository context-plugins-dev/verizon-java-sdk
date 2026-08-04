
# ESIM Request Response

## Structure

`ESIMRequestResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `RequestId` | `String` | Optional | - | String getRequestId() | setRequestId(String requestId) |

## Example

```java
import com.verizon.thingspace.models.ESIMRequestResponse;

ESIMRequestResponse eSIMRequestResponse = new ESIMRequestResponse.Builder()
    .requestId("d1f08526-5443-4054-9a29-4456490ea9f8")
    .build();
```

