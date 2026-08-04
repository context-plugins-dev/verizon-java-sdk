
# Dto Notification Group Request Entity

## Structure

`DtoNotificationGroupRequestEntity`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Description` | `String` | Optional | a short description | String getDescription() | setDescription(String description) |
| `Groupemail` | `String` | Optional | Contact email for the group | String getGroupemail() | setGroupemail(String groupemail) |
| `Name` | `String` | Optional | User defined name of the record | String getName() | setName(String name) |

## Example

```java
import com.verizon.thingspace.models.DtoNotificationGroupRequestEntity;

DtoNotificationGroupRequestEntity dtoNotificationGroupRequestEntity = new DtoNotificationGroupRequestEntity.Builder()
    .description("a short description")
    .groupemail("email@domain.com")
    .name("name of the record")
    .build();
```

