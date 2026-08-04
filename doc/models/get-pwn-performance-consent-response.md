
# Get PWN Performance Consent Response

PWN Performance Consent Response

## Structure

`GetPWNPerformanceConsentResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Consent` | `String` | Optional | PWN Performance Consent Response. | String getConsent() | setConsent(String consent) |

## Example

```java
import com.verizon.thingspace.models.GetPWNPerformanceConsentResponse;

GetPWNPerformanceConsentResponse getPWNPerformanceConsentResponse = new GetPWNPerformanceConsentResponse.Builder()
    .consent("false")
    .build();
```

