
# Dto Delete User Request

## Structure

`DtoDeleteUserRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountname` | `String` | Optional | The numeric account name, which must include leading zeros | String getAccountname() | setAccountname(String accountname) |
| `Id` | `String` | Optional | UUID of the user record, assigned at creation | String getId() | setId(String id) |

## Example

```java
import com.verizon.thingspace.models.DtoDeleteUserRequest;

DtoDeleteUserRequest dtoDeleteUserRequest = new DtoDeleteUserRequest.Builder()
    .accountname("0000123456-00001")
    .id("id2")
    .build();
```

