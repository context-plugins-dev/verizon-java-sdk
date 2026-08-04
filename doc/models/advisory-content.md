
# Advisory Content

DataFrame content variant carrying advisory ITIS codes.

## Structure

`AdvisoryContent`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Advisory` | [`List<AdvisoryItem>`](../../doc/models/containers/advisory-item.md) | Required | The use of ITIS codes interspersed with free text. The complete set of ITIS codes can be found in Volume Two of the SAE J2540 standard.<br><br>**Constraints**: *Minimum Items*: `1`, *Maximum Items*: `100` | List<AdvisoryItem> getAdvisory() | setAdvisory(List<AdvisoryItem> advisory) |

## Example

```java
import com.verizon.thingspace.models.AdvisoryContent;
import com.verizon.thingspace.models.ITISItemContent;
import com.verizon.thingspace.models.ITISItemWrapper;
import com.verizon.thingspace.models.containers.AdvisoryItem;
import java.util.Arrays;

AdvisoryContent advisoryContent = new AdvisoryContent.Builder(
    Arrays.asList(
        AdvisoryItem.fromITISItemWrapper(
            new ITISItemWrapper.Builder(
                new ITISItemContent.Builder(
                    10
                )
                .build()
            )
            .build()
        ),
        AdvisoryItem.fromITISItemWrapper(
            new ITISItemWrapper.Builder(
                new ITISItemContent.Builder(
                    10
                )
                .build()
            )
            .build()
        ),
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
.build();
```

