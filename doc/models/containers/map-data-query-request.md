
# Map Data Query Request

Request structure for querying MAP records. Provide either regionIntersectionPairs (coordinates) or geoJson, not both.

## Class Name

`MapDataQueryRequest`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`ETXMAPMessageIntersectionCoordinates`](../../../doc/models/etxmap-message-intersection-coordinates.md) | MapDataQueryRequest.fromETXMAPMessageIntersectionCoordinates(ETXMAPMessageIntersectionCoordinates eTXMAPMessageIntersectionCoordinates) |
| [`ETXMAPMessageGeoJSONPolygon`](../../../doc/models/etxmap-message-geo-json-polygon.md) | MapDataQueryRequest.fromETXMAPMessageGeoJSONPolygon(ETXMAPMessageGeoJSONPolygon eTXMAPMessageGeoJSONPolygon) |

## ETXMAPMessageIntersectionCoordinates

### Initialization Code

#### Example

```java
MapDataQueryRequest.fromETXMAPMessageIntersectionCoordinates(
        new ETXMAPMessageIntersectionCoordinates.Builder(
            Arrays.asList(
                new RegionIntersectionPair.Builder(
                    5233
                )
                .regionId(100)
                .build()
            )
        )
        .messageStandard(ETXMessageStandardEnum.SAE)
        .expectedType(ETXExpectedTypeEnum.BASE64)
        .pageToken("Y3Vyc29yX3Rva2VuX2V4YW1wbGU=")
        .pageSize(50)
        .build()
    )
```

## ETXMAPMessageGeoJSONPolygon

### Initialization Code

#### Example

```java
MapDataQueryRequest.fromETXMAPMessageGeoJSONPolygon(
        new ETXMAPMessageGeoJSONPolygon.Builder(
            ApiHelper.deserialize("{\"type\":\"Polygon\",\"coordinates\":[[[-77.14,39.01],[-77.03,39.01],[-77.03,38.85],[-77.14,38.85],[-77.14,39.01]]]}")
        )
        .messageStandard(ETXMessageStandardEnum.SAE)
        .expectedType(ETXExpectedTypeEnum.BASE64)
        .pageToken("Y3Vyc29yX3Rva2VuX2V4YW1wbGU=")
        .pageSize(50)
        .build()
    )
```

