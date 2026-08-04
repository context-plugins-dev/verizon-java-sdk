
# Usage Trigger Update Request

## Structure

`UsageTriggerUpdateRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `TriggerName` | `String` | Optional | Usage trigger name | String getTriggerName() | setTriggerName(String triggerName) |
| `AccountName` | `String` | Required | Account name | String getAccountName() | setAccountName(String accountName) |
| `ThresholdValue` | `String` | Optional | The percent of subscribed usage required to activate the trigger, such as 90 or 100. | String getThresholdValue() | setThresholdValue(String thresholdValue) |
| `SmsPhoneNumbers` | `String` | Optional | Comma-separated list of phone numbers to send SMS alerts to. Digits only; no dashes or parentheses, etc. | String getSmsPhoneNumbers() | setSmsPhoneNumbers(String smsPhoneNumbers) |
| `EmailAddresses` | `String` | Optional | Comma-separated list of email addresses to send alerts to. | String getEmailAddresses() | setEmailAddresses(String emailAddresses) |

## Example

```java
import com.verizon.thingspace.models.UsageTriggerUpdateRequest;

UsageTriggerUpdateRequest usageTriggerUpdateRequest = new UsageTriggerUpdateRequest.Builder(
    "0212312345-00001"
)
.triggerName("95% usage alert")
.thresholdValue("95")
.smsPhoneNumbers("5551231234")
.emailAddresses("me@theinternet.com, you@theinternet.com")
.build();
```

