
# Status List

## Structure

`StatusList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Optional | Account name | String getId() | setId(String id) |
| `Status` | `String` | Optional | Success or Fail | String getStatus() | setStatus(String status) |
| `Reason` | `String` | Optional | detailed reason | String getReason() | setReason(String reason) |

## Example

```java
import com.verizon.thingspace.models.StatusList;

StatusList statusList = new StatusList.Builder()
    .id("1223334444-00001")
    .status("Success")
    .reason("Success")
    .build();
```

