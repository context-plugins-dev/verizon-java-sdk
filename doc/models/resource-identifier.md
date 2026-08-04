
# Resource Identifier

The ID of the target to delete, in the format {"id": "dd1682d3-2d80-cefc-f3ee-25154800beff"}.

## Structure

`ResourceIdentifier`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Optional | Target ID. | String getId() | setId(String id) |
| `Imei` | `String` | Optional | Device IMEI. | String getImei() | setImei(String imei) |

## Example

```java
import com.verizon.thingspace.models.ResourceIdentifier;

ResourceIdentifier resourceIdentifier = new ResourceIdentifier.Builder()
    .id("2e61a17d-8fd1-6816-e995-e4c2528bf535")
    .imei("imei6")
    .build();
```

