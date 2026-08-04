
# V2 Triggers Request

## Structure

`V2TriggersRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `TriggerName` | `String` | Optional | The user defined name of the trigger | String getTriggerName() | setTriggerName(String triggerName) |
| `EcpdId` | `String` | Optional | The Enterprise Customer Profile Database ID | String getEcpdId() | setEcpdId(String ecpdId) |
| `TriggerCategory` | [`TriggerCategoryEnum`](../../doc/models/trigger-category-enum.md) | Optional | The type of trigger being created or modified | TriggerCategoryEnum getTriggerCategory() | setTriggerCategory(TriggerCategoryEnum triggerCategory) |
| `DataTrigger` | [`DataTrigger4`](../../doc/models/data-trigger-4.md) | Optional | - | DataTrigger4 getDataTrigger() | setDataTrigger(DataTrigger4 dataTrigger) |
| `Notification` | [`Notificationarray`](../../doc/models/notificationarray.md) | Optional | - | Notificationarray getNotification() | setNotification(Notificationarray notification) |
| `NotificationType` | `String` | Optional | - | String getNotificationType() | setNotificationType(String notificationType) |
| `Callback` | `Boolean` | Optional | - | Boolean getCallback() | setCallback(Boolean callback) |
| `EmailNotification` | `Boolean` | Optional | - | Boolean getEmailNotification() | setEmailNotification(Boolean emailNotification) |
| `NotificationGroupName` | `String` | Optional | - | String getNotificationGroupName() | setNotificationGroupName(String notificationGroupName) |
| `NotificationFrequencyFactor` | `Integer` | Optional | - | Integer getNotificationFrequencyFactor() | setNotificationFrequencyFactor(Integer notificationFrequencyFactor) |
| `NotificationFrequencyInterval` | `String` | Optional | - | String getNotificationFrequencyInterval() | setNotificationFrequencyInterval(String notificationFrequencyInterval) |
| `ExternalEmailRecipients` | `String` | Optional | - | String getExternalEmailRecipients() | setExternalEmailRecipients(String externalEmailRecipients) |
| `SmsNotification` | `Boolean` | Optional | - | Boolean getSmsNotification() | setSmsNotification(Boolean smsNotification) |
| `SmsNumbers` | [`List<V2TriggersRequestSmsNumbers>`](../../doc/models/containers/v2-triggers-request-sms-numbers.md) | Optional | This is List of a container for any-of cases. | List<V2TriggersRequestSmsNumbers> getSmsNumbers() | setSmsNumbers(List<V2TriggersRequestSmsNumbers> smsNumbers) |
| `Reminder` | `Boolean` | Optional | - | Boolean getReminder() | setReminder(Boolean reminder) |
| `Severity` | `String` | Optional | - | String getSeverity() | setSeverity(String severity) |
| `Active` | [`ActiveEnum`](../../doc/models/active-enum.md) | Optional | A flag to indicate of the trigger is active, true, or not, false | ActiveEnum getActive() | setActive(ActiveEnum active) |
| `FilterCriteria` | [`AccountLevelFilter`](../../doc/models/account-level-filter.md) | Optional | - | AccountLevelFilter getFilterCriteria() | setFilterCriteria(AccountLevelFilter filterCriteria) |
| `Condition` | [`V2TriggersRequestCondition`](../../doc/models/containers/v2-triggers-request-condition.md) | Optional | This is a container for any-of cases. | V2TriggersRequestCondition getCondition() | setCondition(V2TriggersRequestCondition condition) |
| `Action` | [`AccountLevelActionEnum`](../../doc/models/account-level-action-enum.md) | Optional | The action taken when trigger conditions are met | AccountLevelActionEnum getAction() | setAction(AccountLevelActionEnum action) |
| `AccountName` | `String` | Optional | The numeric name of the account and must include leading zeroes | String getAccountName() | setAccountName(String accountName) |
| `PricePlanTrigger` | [`PricePlanTrigger1`](../../doc/models/price-plan-trigger-1.md) | Optional | - | PricePlanTrigger1 getPricePlanTrigger() | setPricePlanTrigger(PricePlanTrigger1 pricePlanTrigger) |

## Example

```java
import com.verizon.thingspace.models.AccountLevelActionEnum;
import com.verizon.thingspace.models.AccountLevelFilter;
import com.verizon.thingspace.models.AccountLevelObject;
import com.verizon.thingspace.models.Accountnames;
import com.verizon.thingspace.models.ActiveEnum;
import com.verizon.thingspace.models.ComparitorEnum;
import com.verizon.thingspace.models.ConditionTypeEnum;
import com.verizon.thingspace.models.DataTrigger4;
import com.verizon.thingspace.models.DeviceGroupFilter;
import com.verizon.thingspace.models.DeviceGroupFilterCriteria;
import com.verizon.thingspace.models.Notificationarray;
import com.verizon.thingspace.models.TriggerCategoryEnum;
import com.verizon.thingspace.models.V2TriggersRequest;
import com.verizon.thingspace.models.containers.AccountLevelObjectCondition;
import java.util.Arrays;

V2TriggersRequest v2TriggersRequest = new V2TriggersRequest.Builder()
    .triggerName("name of the trigger")
    .ecpdId("Verizon profile ID")
    .triggerCategory(TriggerCategoryEnum.ACCOUNTUSAGE)
    .dataTrigger(new DataTrigger4.Builder()
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
        .deviceGroup(new DeviceGroupFilterCriteria.Builder()
            .filterCriteria(new DeviceGroupFilter.Builder()
                .deviceGroupName("deviceGroupName4")
                .individualOrCombined("IndividualOrCombined4")
                .accountName("accountName0")
                .build())
            .build())
        .conditionType(ConditionTypeEnum.AGING)
        .comparitor(ComparitorEnum.EQ)
        .threshold(222)
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
    .action(AccountLevelActionEnum.NOTIFY)
    .accountName("0000123456-00001")
    .build();
```

