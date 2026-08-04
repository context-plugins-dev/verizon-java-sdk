
# Fota V2 Callback Registration Request

Callback URL registration.

## Structure

`FotaV2CallbackRegistrationRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Url` | `String` | Optional | Callback URL for an subscribed service. | String getUrl() | setUrl(String url) |

## Example

```java
import com.verizon.thingspace.models.FotaV2CallbackRegistrationRequest;

FotaV2CallbackRegistrationRequest fotaV2CallbackRegistrationRequest = new FotaV2CallbackRegistrationRequest.Builder()
    .url("https://255.255.11.135:50559/CallbackListener/FirmwareServiceMessages.asmx")
    .build();
```

