
# Generate External ID Result

A new external ID.

## Structure

`GenerateExternalIDResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Externalid` | `String` | Optional | Newly created security string. | String getExternalid() | setExternalid(String externalid) |

## Example

```java
import com.verizon.thingspace.models.GenerateExternalIDResult;

GenerateExternalIDResult generateExternalIDResult = new GenerateExternalIDResult.Builder()
    .externalid("ZlJnih8BfqsosZrEEkfPuR3aGOk2i-HIr6tXN275ioJF6bezIrQB9EbzpTRep8J7RmV7QH==")
    .build();
```

