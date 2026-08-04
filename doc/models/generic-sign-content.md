
# Generic Sign Content

DataFrame content variant carrying generic sign information.

## Structure

`GenericSignContent`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `GenericSign` | [`List<TextPhraseOrITIS>`](../../doc/models/containers/text-phrase-or-itis.md) | Required | A data frame to allow sequences of ITIS codes, short text strings, and numerical values to be expressed in the normal ITIS vocabulary method and pattern. Note that the allowed text strings are more limited than the normal ITIS format in order to conserve bandwidth.<br><br>**Constraints**: *Minimum Items*: `1`, *Maximum Items*: `16` | List<TextPhraseOrITIS> getGenericSign() | setGenericSign(List<TextPhraseOrITIS> genericSign) |

## Example

```java
import com.verizon.thingspace.models.GenericSignContent;
import com.verizon.thingspace.models.ITISItemContent;
import com.verizon.thingspace.models.ITISItemWrapper;
import com.verizon.thingspace.models.containers.TextPhraseOrITIS;
import java.util.Arrays;

GenericSignContent genericSignContent = new GenericSignContent.Builder(
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
.build();
```

