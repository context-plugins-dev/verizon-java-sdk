
# Account Level Create Trigger Request

## Structure

`AccountLevelCreateTriggerRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `TriggerName` | `String` | Optional | The user defined name of the trigger | String getTriggerName() | setTriggerName(String triggerName) |
| `EcpdId` | `String` | Optional | The Enterprise Customer Profile Database ID | String getEcpdId() | setEcpdId(String ecpdId) |
| `TriggerCategory` | [`TriggerCategoryEnum`](../../doc/models/trigger-category-enum.md) | Optional | The type of trigger being created or modified | TriggerCategoryEnum getTriggerCategory() | setTriggerCategory(TriggerCategoryEnum triggerCategory) |
| `DataTrigger` | [`DataTrigger`](../../doc/models/data-trigger.md) | Optional | - | DataTrigger getDataTrigger() | setDataTrigger(DataTrigger dataTrigger) |
| `Notification` | [`Notificationarray`](../../doc/models/notificationarray.md) | Optional | - | Notificationarray getNotification() | setNotification(Notificationarray notification) |
| `NotificationType` | `String` | Optional | - | String getNotificationType() | setNotificationType(String notificationType) |
| `Callback` | `Boolean` | Optional | - | Boolean getCallback() | setCallback(Boolean callback) |
| `EmailNotification` | `Boolean` | Optional | - | Boolean getEmailNotification() | setEmailNotification(Boolean emailNotification) |
| `NotificationGroupName` | `String` | Optional | - | String getNotificationGroupName() | setNotificationGroupName(String notificationGroupName) |
| `NotificationFrequencyFactor` | `Integer` | Optional | - | Integer getNotificationFrequencyFactor() | setNotificationFrequencyFactor(Integer notificationFrequencyFactor) |
| `NotificationFrequencyInterval` | `String` | Optional | - | String getNotificationFrequencyInterval() | setNotificationFrequencyInterval(String notificationFrequencyInterval) |
| `ExternalEmailRecipients` | `String` | Optional | - | String getExternalEmailRecipients() | setExternalEmailRecipients(String externalEmailRecipients) |
| `SmsNotification` | `Boolean` | Optional | - | Boolean getSmsNotification() | setSmsNotification(Boolean smsNotification) |
| `SmsNumbers` | [`List<AccountLevelCreateTriggerRequestSmsNumbers>`](../../doc/models/containers/account-level-create-trigger-request-sms-numbers.md) | Optional | This is List of a container for any-of cases. | List<AccountLevelCreateTriggerRequestSmsNumbers> getSmsNumbers() | setSmsNumbers(List<AccountLevelCreateTriggerRequestSmsNumbers> smsNumbers) |
| `Reminder` | `Boolean` | Optional | - | Boolean getReminder() | setReminder(Boolean reminder) |
| `Severity` | `String` | Optional | - | String getSeverity() | setSeverity(String severity) |
| `Active` | [`ActiveEnum`](../../doc/models/active-enum.md) | Optional | A flag to indicate of the trigger is active, true, or not, false | ActiveEnum getActive() | setActive(ActiveEnum active) |

## Example

```java
import com.verizon.thingspace.models.AccountLevelActionEnum;
import com.verizon.thingspace.models.AccountLevelCreateTriggerRequest;
import com.verizon.thingspace.models.AccountLevelFilter;
import com.verizon.thingspace.models.AccountLevelObject;
import com.verizon.thingspace.models.Accountnames;
import com.verizon.thingspace.models.ActiveEnum;
import com.verizon.thingspace.models.ConditionTypeEnum;
import com.verizon.thingspace.models.DataTrigger;
import com.verizon.thingspace.models.Notificationarray;
import com.verizon.thingspace.models.TriggerCategoryEnum;
import com.verizon.thingspace.models.containers.AccountLevelObjectCondition;
import java.util.Arrays;

AccountLevelCreateTriggerRequest accountLevelCreateTriggerRequest = new AccountLevelCreateTriggerRequest.Builder()
    .triggerName("name of the trigger")
    .ecpdId("Verizon profile ID")
    .triggerCategory(TriggerCategoryEnum.ACCOUNTUSAGE)
    .dataTrigger(new DataTrigger.Builder()
        .accountLevel(new AccountLevelObject.Builder()
            .filterCriteria(new AccountLevelFilter.Builder()
                .separateOrCombined("separateOrCombined4")
                .accountNames(new Accountnames.Builder()
                    .accountNameList(Arrays.asList(
                        "accountNameList7",
                        "accountNameList8",
                        "accountNameList9"
                    ))
                    .build())
                .build())
            .condition(AccountLevelObjectCondition.fromConditionType(
                ConditionTypeEnum.INDIVIDUAL
            ))
            .action(AccountLevelActionEnum.SUSPEND)
            .build())
        .build())
    .notification(new Notificationarray.Builder()
        .notificationType("notificationType8")
        .callback(false)
        .emailNotification(false)
        .notificationGroupName("notificationGroupName6")
        .notificationFrequencyFactor(22)
        .build())
    .notificationType("PerEvent")
    .callback(true)
    .emailNotification(false)
    .notificationGroupName("Notification Group Name (User defined)")
    .notificationFrequencyFactor(3)
    .notificationFrequencyInterval("Daily")
    .externalEmailRecipients("Email addresses")
    .smsNotification(true)
    .reminder(true)
    .severity("Notify")
    .active(ActiveEnum.ENUM_TRUE)
    .build();
```

