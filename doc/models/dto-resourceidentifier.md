
# Dto Resourceidentifier

## Structure

`DtoResourceidentifier`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Optional | UUID of the user record, assigned at creation | String getId() | setId(String id) |

## Example

```java
import com.verizon.thingspace.models.DtoResourceidentifier;

DtoResourceidentifier dtoResourceidentifier = new DtoResourceidentifier.Builder()
    .id("id0")
    .build();
```

