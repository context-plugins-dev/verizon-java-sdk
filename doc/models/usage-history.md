
# Usage History

## Structure

`UsageHistory`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `BytesUsed` | `Integer` | Optional | - | Integer getBytesUsed() | setBytesUsed(Integer bytesUsed) |
| `Serviceplan` | `String` | Optional | - | String getServiceplan() | setServiceplan(String serviceplan) |
| `SmsUsed` | `Integer` | Optional | - | Integer getSmsUsed() | setSmsUsed(Integer smsUsed) |
| `MoSMS` | `Integer` | Optional | - | Integer getMoSMS() | setMoSMS(Integer moSMS) |
| `MtSMS` | `Integer` | Optional | - | Integer getMtSMS() | setMtSMS(Integer mtSMS) |
| `Source` | `String` | Optional | - | String getSource() | setSource(String source) |
| `EventDateTime` | `LocalDateTime` | Optional | - | LocalDateTime getEventDateTime() | setEventDateTime(LocalDateTime eventDateTime) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.UsageHistory;

UsageHistory usageHistory = new UsageHistory.Builder()
    .bytesUsed(3072)
    .serviceplan("The serviceplan name")
    .smsUsed(176)
    .moSMS(230)
    .mtSMS(18)
    .source("Raw Usage")
    .eventDateTime(DateTimeHelper.fromRfc8601DateTime("2021-08-15T00:00:00Z"))
    .build();
```

