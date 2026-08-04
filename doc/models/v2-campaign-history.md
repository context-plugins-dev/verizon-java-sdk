
# V2 Campaign History

Campaign history details.

## Structure

`V2CampaignHistory`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `HasMoreData` | `boolean` | Required | Has more report flag. | boolean getHasMoreData() | setHasMoreData(boolean hasMoreData) |
| `LastSeenCampaignId` | `String` | Optional | Campaign identifier. | String getLastSeenCampaignId() | setLastSeenCampaignId(String lastSeenCampaignId) |
| `CampaignList` | [`List<V2CampaignMetaInfo>`](../../doc/models/v2-campaign-meta-info.md) | Required | Software upgrade list. | List<V2CampaignMetaInfo> getCampaignList() | setCampaignList(List<V2CampaignMetaInfo> campaignList) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.V2CampaignHistory;
import com.verizon.thingspace.models.V2CampaignMetaInfo;
import com.verizon.thingspace.models.V2TimeWindow;
import java.util.Arrays;

V2CampaignHistory v2CampaignHistory = new V2CampaignHistory.Builder(
    true,
    Arrays.asList(
        new V2CampaignMetaInfo.Builder(
            "0402196254-00001",
            "60b5d639-ccdc-4db8-8824-069bd94c95bf",
            "FOTA_Verizon_Model-A_02To03_HF",
            "HTTP",
            "FOTA_Verizon_Model-A_00To01_HF",
            "FOTA_Verizon_Model-A_02To03_HF",
            "Verizon",
            "Model-A",
            DateTimeHelper.fromSimpleDate("2020-08-21"),
            DateTimeHelper.fromSimpleDate("2020-08-22"),
            "CampaignEnded"
        )
        .campaignName("FOTA_Verizon_Upgrade")
        .downloadAfterDate(DateTimeHelper.fromSimpleDate("2020-08-21"))
        .downloadTimeWindowList(Arrays.asList(
                new V2TimeWindow.Builder(
                    20,
                    21
                )
                .build()
            ))
        .installAfterDate(DateTimeHelper.fromSimpleDate("2020-08-21"))
        .installTimeWindowList(Arrays.asList(
                new V2TimeWindow.Builder(
                    22,
                    23
                )
                .build()
            ))
        .build()
    )
)
.lastSeenCampaignId("60b5d639-ccdc-4db8-8824-069bd94c95bf")
.build();
```

