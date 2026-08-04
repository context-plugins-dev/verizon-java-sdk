
# Speed Limit Content

DataFrame content variant carrying speed limit information.

## Structure

`SpeedLimitContent`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SpeedLimit` | [`List<TextPhraseOrITIS>`](../../doc/models/containers/text-phrase-or-itis.md) | Required | A data frame to allow sequences of ITIS codes, short text strings, and numerical values to be expressed in the normal ITIS vocabulary method and pattern. Note that the allowed text strings are more limited than the normal ITIS format in order to conserve bandwidth.<br><br>**Constraints**: *Minimum Items*: `1`, *Maximum Items*: `16` | List<TextPhraseOrITIS> getSpeedLimit() | setSpeedLimit(List<TextPhraseOrITIS> speedLimit) |

## Example

```java
import com.verizon.thingspace.models.ITISItemContent;
import com.verizon.thingspace.models.ITISItemWrapper;
import com.verizon.thingspace.models.SpeedLimitContent;
import com.verizon.thingspace.models.containers.TextPhraseOrITIS;
import java.util.Arrays;

SpeedLimitContent speedLimitContent = new SpeedLimitContent.Builder(
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

