
# Group Name

## Structure

`GroupName`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Default` | `String` | Optional | - | String getDefault() | setDefault(String mDefault) |

## Example

```java
import com.verizon.thingspace.models.GroupName;

GroupName groupName = new GroupName.Builder()
    .mDefault("0000123456-00001")
    .build();
```

