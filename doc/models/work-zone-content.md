
# Work Zone Content

DataFrame content variant carrying work zone information.

## Structure

`WorkZoneContent`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `WorkZone` | [`List<TextPhraseOrITIS>`](../../doc/models/containers/text-phrase-or-itis.md) | Required | A data frame to allow sequences of ITIS codes, short text strings, and numerical values to be expressed in the normal ITIS vocabulary method and pattern. Note that the allowed text strings are more limited than the normal ITIS format in order to conserve bandwidth.<br><br>**Constraints**: *Minimum Items*: `1`, *Maximum Items*: `16` | List<TextPhraseOrITIS> getWorkZone() | setWorkZone(List<TextPhraseOrITIS> workZone) |

## Example

```java
import com.verizon.thingspace.models.ITISItemContent;
import com.verizon.thingspace.models.ITISItemWrapper;
import com.verizon.thingspace.models.WorkZoneContent;
import com.verizon.thingspace.models.containers.TextPhraseOrITIS;
import java.util.Arrays;

WorkZoneContent workZoneContent = new WorkZoneContent.Builder(
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

