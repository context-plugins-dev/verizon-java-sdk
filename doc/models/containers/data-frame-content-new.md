
# Data Frame Content New

## Class Name

`DataFrameContentNew`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`ContentFrictionInfo`](../../../doc/models/content-friction-info.md) | DataFrameContentNew.fromContentFrictionInfo(ContentFrictionInfo contentFrictionInfo) |

## ContentFrictionInfo

### Initialization Code

#### Example

```java
DataFrameContentNew.fromContentFrictionInfo(
        new ContentFrictionInfo.Builder(
            new FrictionInformation.Builder(
                DescriptionOfRoadSurface.fromDescriptionOfRoadSurfacePortlandCement(
                    new DescriptionOfRoadSurfacePortlandCement.Builder(
                        new PortlandCement.Builder()
                            .type(Type6Enum.TRAVELED)
                            .build()
                    )
                    .build()
                )
            )
            .build()
        )
        .build()
    )
```

