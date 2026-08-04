
# Limits

List of limitations. These limitations can be used for making the trigger condition more precise by defining speed and motion direction requirements to be met before the messages are sent out.

## Class Name

`Limits`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`SpeedItem`](../../../doc/models/speed-item.md) | Limits.fromSpeedItem(SpeedItem speedItem) |
| [`HeadingItem`](../../../doc/models/heading-item.md) | Limits.fromHeadingItem(HeadingItem headingItem) |

## SpeedItem

### Initialization Code

#### Example

```java
Limits.fromSpeedItem(
        new SpeedItem.Builder(
            new SpeedRange.Builder(
                64.76D,
                138.18D
            )
            .build()
        )
        .build()
    )
```

## HeadingItem

### Initialization Code

#### Example

```java
Limits.fromHeadingItem(
        new HeadingItem.Builder(
            new HeadingRange.Builder(
                70.7D,
                144.12D
            )
            .build()
        )
        .build()
    )
```

