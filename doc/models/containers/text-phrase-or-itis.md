
# Text Phrase or ITIS

A data frame to allow sequences of ITIS codes, short text strings, and numerical values to be expressed in the normal ITIS vocabulary method and pattern. Note that the allowed text strings are more limited than the normal ITIS format in order to conserve bandwidth.

## Class Name

`TextPhraseOrITIS`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`ITISItemWrapper`](../../../doc/models/itis-item-wrapper.md) | TextPhraseOrITIS.fromITISItemWrapper(ITISItemWrapper iTISItemWrapper) |
| [`TextPhraseItemWrapper`](../../../doc/models/text-phrase-item-wrapper.md) | TextPhraseOrITIS.fromTextPhraseItemWrapper(TextPhraseItemWrapper textPhraseItemWrapper) |

## ITISItemWrapper

### Initialization Code

#### Example

```java
TextPhraseOrITIS.fromITISItemWrapper(
        new ITISItemWrapper.Builder(
            new ITISItemContent.Builder(
                10
            )
            .build()
        )
        .build()
    )
```

## TextPhraseItemWrapper

### Initialization Code

#### Example

```java
TextPhraseOrITIS.fromTextPhraseItemWrapper(
        new TextPhraseItemWrapper.Builder(
            new TextPhraseItemContent.Builder(
                "text2"
            )
            .build()
        )
        .build()
    )
```

