
# Notification Group Name Trigger Attribute

Notification group name trigger attribute.

## Structure

`NotificationGroupNameTriggerAttribute`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Key` | `String` | Optional | If present, the NotificationGroupName will be listed here. | String getKey() | setKey(String key) |

## Example

```java
import com.verizon.thingspace.models.NotificationGroupNameTriggerAttribute;

NotificationGroupNameTriggerAttribute notificationGroupNameTriggerAttribute = new NotificationGroupNameTriggerAttribute.Builder()
    .key("NotificationGroupName")
    .build();
```

