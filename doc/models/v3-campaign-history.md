
# V3 Campaign History

Campaign history.

## Structure

`V3CampaignHistory`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `HasMoreData` | `boolean` | Required | Has more report flag? | boolean getHasMoreData() | setHasMoreData(boolean hasMoreData) |
| `LastSeenCampaignId` | `String` | Optional | Campaign identifier. | String getLastSeenCampaignId() | setLastSeenCampaignId(String lastSeenCampaignId) |
| `CampaignList` | [`List<V3CampaignMetaInfo>`](../../doc/models/v3-campaign-meta-info.md) | Required | Firmware upgrade list. | List<V3CampaignMetaInfo> getCampaignList() | setCampaignList(List<V3CampaignMetaInfo> campaignList) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.CampaignMetaInfoProtocolEnum;
import com.verizon.thingspace.models.V3CampaignHistory;
import com.verizon.thingspace.models.V3CampaignMetaInfo;
import com.verizon.thingspace.models.V3TimeWindow;
import java.util.Arrays;

V3CampaignHistory v3CampaignHistory = new V3CampaignHistory.Builder(
    true,
    Arrays.asList(
        new V3CampaignMetaInfo.Builder(
            "0000123456-00001",
            "60b5d639-ccdc-4db8-8824-069bd94c95bf",
            "Verizon",
            "Model-A",
            DateTimeHelper.fromSimpleDate("2020-08-21"),
            DateTimeHelper.fromSimpleDate("2020-08-22"),
            "CampaignEnded"
        )
        .campaignName("FOTA_Verizon_Upgrade")
        .firmwareName("firmwareName6")
        .firmwareFrom("firmwareFrom6")
        .firmwareTo("firmwareTo6")
        .protocol(CampaignMetaInfoProtocolEnum.LW_M2M)
        .campaignTimeWindowList(Arrays.asList(
                new V3TimeWindow.Builder(
                    20,
                    21
                )
                .build()
            ))
        .build()
    )
)
.lastSeenCampaignId("60b5d639-ccdc-4db8-8824-069bd94c95bf")
.build();
```

