
# Callback Summary

Registered callback information.

## Structure

`CallbackSummary`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Url` | `String` | Optional | Callback URL for an subscribed service. | String getUrl() | setUrl(String url) |

## Example

```java
import com.verizon.thingspace.models.CallbackSummary;

CallbackSummary callbackSummary = new CallbackSummary.Builder()
    .url("http://10.120.102.183:50559/CallbackListener/FirmwareServiceMessages.asmx")
    .build();
```

