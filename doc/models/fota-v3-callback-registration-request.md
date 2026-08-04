
# Fota V3 Callback Registration Request

Callback URL where the listening service is running.

## Structure

`FotaV3CallbackRegistrationRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Url` | `String` | Optional | Callback URL for an subscribed service. | String getUrl() | setUrl(String url) |

## Example

```java
import com.verizon.thingspace.models.FotaV3CallbackRegistrationRequest;

FotaV3CallbackRegistrationRequest fotaV3CallbackRegistrationRequest = new FotaV3CallbackRegistrationRequest.Builder()
    .url("https://255.255.11.135:50559/CallbackListener/FirmwareServiceMessages.asmx")
    .build();
```

