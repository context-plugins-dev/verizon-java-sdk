
# Change PWN Device Ipaddress Response

Response to change PWN device ip address.

## Structure

`ChangePWNDeviceIpaddressResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `RequestId` | `String` | Optional | A unique string that associates the request with the results that are sent via a callback service. | String getRequestId() | setRequestId(String requestId) |

## Example

```java
import com.verizon.thingspace.models.ChangePWNDeviceIpaddressResponse;

ChangePWNDeviceIpaddressResponse changePWNDeviceIpaddressResponse = new ChangePWNDeviceIpaddressResponse.Builder()
    .requestId("24da9f9a-d110-4a54-86b4-93fb76aab83c")
    .build();
```

