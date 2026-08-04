
# Data Frame Content

## Class Name

`DataFrameContent`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`AdvisoryContent`](../../../doc/models/advisory-content.md) | DataFrameContent.fromAdvisoryContent(AdvisoryContent advisoryContent) |
| [`WorkZoneContent`](../../../doc/models/work-zone-content.md) | DataFrameContent.fromWorkZoneContent(WorkZoneContent workZoneContent) |
| [`GenericSignContent`](../../../doc/models/generic-sign-content.md) | DataFrameContent.fromGenericSignContent(GenericSignContent genericSignContent) |
| [`SpeedLimitContent`](../../../doc/models/speed-limit-content.md) | DataFrameContent.fromSpeedLimitContent(SpeedLimitContent speedLimitContent) |
| [`ExitServiceContent`](../../../doc/models/exit-service-content.md) | DataFrameContent.fromExitServiceContent(ExitServiceContent exitServiceContent) |

## AdvisoryContent

### Initialization Code

#### Example

```java
DataFrameContent.fromAdvisoryContent(
        new AdvisoryContent.Builder(
            Arrays.asList(
                AdvisoryItem.fromITISItemWrapper(
                    new ITISItemWrapper.Builder(
                        new ITISItemContent.Builder(
                            10
                        )
                        .build()
                    )
                    .build()
                )
            )
        )
        .build()
    )
```

## WorkZoneContent

### Initialization Code

#### Example

```java
DataFrameContent.fromWorkZoneContent(
        new WorkZoneContent.Builder(
            Arrays.asList(
                TextPhraseOrITIS.fromITISItemWrapper(
                    new ITISItemWrapper.Builder(
                        new ITISItemContent.Builder(
                            10
                        )
                        .build()
                    )
                    .build()
                ),
                TextPhraseOrITIS.fromITISItemWrapper(
                    new ITISItemWrapper.Builder(
                        new ITISItemContent.Builder(
                            10
                        )
                        .build()
                    )
                    .build()
                )
            )
        )
        .build()
    )
```

## GenericSignContent

### Initialization Code

#### Example

```java
DataFrameContent.fromGenericSignContent(
        new GenericSignContent.Builder(
            Arrays.asList(
                TextPhraseOrITIS.fromITISItemWrapper(
                    new ITISItemWrapper.Builder(
                        new ITISItemContent.Builder(
                            10
                        )
                        .build()
                    )
                    .build()
                )
            )
        )
        .build()
    )
```

## SpeedLimitContent

### Initialization Code

#### Example

```java
DataFrameContent.fromSpeedLimitContent(
        new SpeedLimitContent.Builder(
            Arrays.asList(
                TextPhraseOrITIS.fromITISItemWrapper(
                    new ITISItemWrapper.Builder(
                        new ITISItemContent.Builder(
                            10
                        )
                        .build()
                    )
                    .build()
                ),
                TextPhraseOrITIS.fromITISItemWrapper(
                    new ITISItemWrapper.Builder(
                        new ITISItemContent.Builder(
                            10
                        )
                        .build()
                    )
                    .build()
                )
            )
        )
        .build()
    )
```

## ExitServiceContent

### Initialization Code

#### Example

```java
DataFrameContent.fromExitServiceContent(
        new ExitServiceContent.Builder(
            Arrays.asList(
                TextPhraseOrITIS.fromITISItemWrapper(
                    new ITISItemWrapper.Builder(
                        new ITISItemContent.Builder(
                            10
                        )
                        .build()
                    )
                    .build()
                )
            )
        )
        .build()
    )
```

