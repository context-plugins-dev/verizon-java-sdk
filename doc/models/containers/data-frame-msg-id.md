
# Data Frame Msg Id

## Class Name

`DataFrameMsgId`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`FurtherInfoMsgId`](../../../doc/models/further-info-msg-id.md) | DataFrameMsgId.fromFurtherInfoMsgId(FurtherInfoMsgId furtherInfoMsgId) |
| [`RoadSignMsgId`](../../../doc/models/road-sign-msg-id.md) | DataFrameMsgId.fromRoadSignMsgId(RoadSignMsgId roadSignMsgId) |

## FurtherInfoMsgId

### Initialization Code

#### Example

```java
DataFrameMsgId.fromFurtherInfoMsgId(
        new FurtherInfoMsgId.Builder(
            "1101"
        )
        .build()
    )
```

## RoadSignMsgId

### Initialization Code

#### Example

```java
DataFrameMsgId.fromRoadSignMsgId(
        new RoadSignMsgId.Builder(
            new RoadSignID.Builder(
                new RoadSignPosition.Builder(
                    14,
                    172
                )
                .build(),
                "1101"
            )
            .build()
        )
        .build()
    )
```

