
# Usage Request Response

## Structure

`UsageRequestResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `RequestId` | `String` | Optional | - | String getRequestId() | setRequestId(String requestId) |

## Example

```java
import com.verizon.thingspace.models.UsageRequestResponse;

UsageRequestResponse usageRequestResponse = new UsageRequestResponse.Builder()
    .requestId("be1b5958-3e11-41db-9abd-b1b7618c0035")
    .build();
```

