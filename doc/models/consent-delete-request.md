
# Consent Delete Request

## Structure

`ConsentDeleteRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Optional | Account identifier. | String getAccountName() | setAccountName(String accountName) |
| `DeviceList` | `List<String>` | Optional | Device ID list. | List<String> getDeviceList() | setDeviceList(List<String> deviceList) |

## Example

```java
import com.verizon.thingspace.models.ConsentDeleteRequest;
import java.util.Arrays;

ConsentDeleteRequest consentDeleteRequest = new ConsentDeleteRequest.Builder()
    .accountName("MyAccount-1")
    .deviceList(Arrays.asList(
        "deviceList8",
        "deviceList9"
    ))
    .build();
```

