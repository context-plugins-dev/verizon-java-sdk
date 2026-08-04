
# Advisory Item

The use of ITIS codes interspersed with free text. The complete set of ITIS codes can be found in Volume Two of the SAE J2540 standard.

## Class Name

`AdvisoryItem`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`ITISItemWrapper`](../../../doc/models/itis-item-wrapper.md) | AdvisoryItem.fromITISItemWrapper(ITISItemWrapper iTISItemWrapper) |
| [`TextItemWrapper`](../../../doc/models/text-item-wrapper.md) | AdvisoryItem.fromTextItemWrapper(TextItemWrapper textItemWrapper) |

## ITISItemWrapper

### Initialization Code

#### Example

```java
AdvisoryItem.fromITISItemWrapper(
        new ITISItemWrapper.Builder(
            new ITISItemContent.Builder(
                10
            )
            .build()
        )
        .build()
    )
```

## TextItemWrapper

### Initialization Code

#### Example

```java
AdvisoryItem.fromTextItemWrapper(
        new TextItemWrapper.Builder(
            new TextItemContent.Builder(
                "text2"
            )
            .build()
        )
        .build()
    )
```

