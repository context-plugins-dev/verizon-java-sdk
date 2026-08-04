
# Region Intersection Pair

Specific region and intersection identification pair

## Structure

`RegionIntersectionPair`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `RegionId` | `Integer` | Optional | The region identifier code (0-65535)<br><br>**Default**: `0`<br><br>**Constraints**: `>= 0`, `<= 65535` | Integer getRegionId() | setRegionId(Integer regionId) |
| `IntersectionId` | `int` | Required | The intersection identifier code (0-65535)<br><br>**Constraints**: `>= 0`, `<= 65535` | int getIntersectionId() | setIntersectionId(int intersectionId) |

## Example

```java
import com.verizon.thingspace.models.RegionIntersectionPair;

RegionIntersectionPair regionIntersectionPair = new RegionIntersectionPair.Builder(
    5233
)
.regionId(100)
.build();
```

