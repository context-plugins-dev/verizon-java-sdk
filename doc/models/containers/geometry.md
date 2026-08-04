
# Geometry

## Class Name

`Geometry`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`LineString`](../../../doc/models/line-string.md) | Geometry.fromLineString(LineString lineString) |
| [`Polygon`](../../../doc/models/polygon.md) | Geometry.fromPolygon(Polygon polygon) |
| [`MultiLineString`](../../../doc/models/multi-line-string.md) | Geometry.fromMultiLineString(MultiLineString multiLineString) |
| [`MultiPolygon`](../../../doc/models/multi-polygon.md) | Geometry.fromMultiPolygon(MultiPolygon multiPolygon) |

## LineString

### Initialization Code

#### Example

```java
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
    )
```

## Polygon

### Initialization Code

#### Example

```java
Geometry.fromPolygon(
        new Polygon.Builder(
            Type3Enum.POLYGON,
            Arrays.asList(
                Arrays.asList(
                    Arrays.asList(
                        180D
                    )
                )
            )
        )
        .build()
    )
```

## MultiLineString

### Initialization Code

#### Example

```java
Geometry.fromMultiLineString(
        new MultiLineString.Builder(
            Type4Enum.MULTILINESTRING,
            Arrays.asList(
                Arrays.asList(
                    Arrays.asList(
                        180D,
                        180D
                    ),
                    Arrays.asList(
                        180D,
                        180D
                    )
                ),
                Arrays.asList(
                    Arrays.asList(
                        180D,
                        180D
                    ),
                    Arrays.asList(
                        180D,
                        180D
                    )
                )
            )
        )
        .build()
    )
```

## MultiPolygon

### Initialization Code

#### Example

```java
Geometry.fromMultiPolygon(
        new MultiPolygon.Builder(
            Type5Enum.MULTIPOLYGON,
            Arrays.asList(
                Arrays.asList(
                    Arrays.asList(
                        Arrays.asList(
                            46.55D
                        )
                    )
                )
            )
        )
        .build()
    )
```

