
# Feature Item

## Structure

`FeatureItem`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | [`Type1Enum`](../../doc/models/type-1-enum.md) | Required | - | Type1Enum getType() | setType(Type1Enum type) |
| `Geometry` | [`Geometry`](../../doc/models/containers/geometry.md) | Required | - | Geometry getGeometry() | setGeometry(Geometry geometry) |
| `Properties` | `Object` | Required | Properties object for a GeoJSON Feature (no additional properties allowed). | Object getProperties() | setProperties(Object properties) |

## Example

```java
import com.verizon.thingspace.ApiHelper;
import com.verizon.thingspace.models.FeatureItem;
import com.verizon.thingspace.models.LineString;
import com.verizon.thingspace.models.Type1Enum;
import com.verizon.thingspace.models.Type2Enum;
import com.verizon.thingspace.models.containers.Geometry;
import java.io.IOException;
import java.util.Arrays;

FeatureItem featureItem = new FeatureItem.Builder(
    Type1Enum.FEATURE,
    Geometry.fromLineString(
        new LineString.Builder(
            Type2Enum.LINESTRING,
            Arrays.asList(
                Arrays.asList(
                    51.53D,
                    51.54D
                ),
                Arrays.asList(
                    51.53D,
                    51.54D
                )
            )
        )
        .build()
    ),
    ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}")
)
.build();
```

