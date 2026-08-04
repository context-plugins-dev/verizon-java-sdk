
# Geo Fence

The GeoJSON representation of geofence. Geofence supports the following geometry types: LineString, Polygon, MultiLineString, and MultiPolygon. The system only supports a single Feature in the FeatureCollection, so only one Line, Polygon, MultiLine or MultiPolygon can be defined within one Geofencing configuration.

## Structure

`GeoFence`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | [`TypeEnum`](../../doc/models/type-enum.md) | Required | - | TypeEnum getType() | setType(TypeEnum type) |
| `Features` | [`List<FeatureItem>`](../../doc/models/feature-item.md) | Required | **Constraints**: *Minimum Items*: `1`, *Maximum Items*: `1` | List<FeatureItem> getFeatures() | setFeatures(List<FeatureItem> features) |

## Example

```java
import com.verizon.thingspace.ApiHelper;
import com.verizon.thingspace.models.FeatureItem;
import com.verizon.thingspace.models.GeoFence;
import com.verizon.thingspace.models.LineString;
import com.verizon.thingspace.models.Type1Enum;
import com.verizon.thingspace.models.Type2Enum;
import com.verizon.thingspace.models.TypeEnum;
import com.verizon.thingspace.models.containers.Geometry;
import java.io.IOException;
import java.util.Arrays;

GeoFence geoFence = new GeoFence.Builder(
    TypeEnum.FEATURECOLLECTION,
    Arrays.asList(
        new FeatureItem.Builder(
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
        .build()
    )
)
.build();
```

