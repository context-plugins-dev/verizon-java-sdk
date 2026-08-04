
# ETXMAP Message Intersection Coordinates

Query MAP records using specific region and intersection identifier pairs

## Structure

`ETXMAPMessageIntersectionCoordinates`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `MessageStandard` | [`ETXMessageStandardEnum`](../../doc/models/etx-message-standard-enum.md) | Optional | V2X messaging standard selection. Accepted values are 'sae' (SAE J2735) and 'etsi' (ETSI TS 103 301).<br><br>**Default**: `ETXMessageStandardEnum.SAE`<br><br>**Constraints**: *Maximum Length*: `4`, *Pattern*: `^(etsi\|sae)$` | ETXMessageStandardEnum getMessageStandard() | setMessageStandard(ETXMessageStandardEnum messageStandard) |
| `RegionIntersectionPairs` | [`List<RegionIntersectionPair>`](../../doc/models/region-intersection-pair.md) | Required | List of region and intersection ID pairs to retrieve MAP messages for.<br><br>**Constraints**: *Maximum Items*: `200` | List<RegionIntersectionPair> getRegionIntersectionPairs() | setRegionIntersectionPairs(List<RegionIntersectionPair> regionIntersectionPairs) |
| `ExpectedType` | [`ETXExpectedTypeEnum`](../../doc/models/etx-expected-type-enum.md) | Optional | The format of the payload in the response body.<br><br>**Default**: `ETXExpectedTypeEnum.BASE64`<br><br>**Constraints**: *Maximum Length*: `6`, *Pattern*: `^(BASE64\|JSON)$` | ETXExpectedTypeEnum getExpectedType() | setExpectedType(ETXExpectedTypeEnum expectedType) |
| `PageToken` | `String` | Optional | Base64 encoded token used to retrieve the next page of results<br><br>**Constraints**: *Maximum Length*: `500`, *Pattern*: `^[A-Za-z0-9+/]+=*$` | String getPageToken() | setPageToken(String pageToken) |
| `PageSize` | `Integer` | Optional | Maximum number of records to return in a single page<br><br>**Default**: `200`<br><br>**Constraints**: `>= 1`, `<= 500` | Integer getPageSize() | setPageSize(Integer pageSize) |

## Example

```java
import com.verizon.thingspace.models.ETXExpectedTypeEnum;
import com.verizon.thingspace.models.ETXMAPMessageIntersectionCoordinates;
import com.verizon.thingspace.models.ETXMessageStandardEnum;
import com.verizon.thingspace.models.RegionIntersectionPair;
import java.util.Arrays;

ETXMAPMessageIntersectionCoordinates eTXMAPMessageIntersectionCoordinates = new ETXMAPMessageIntersectionCoordinates.Builder(
    Arrays.asList(
        new RegionIntersectionPair.Builder(
            5233
        )
        .regionId(100)
        .build()
    )
)
.messageStandard(ETXMessageStandardEnum.SAE)
.expectedType(ETXExpectedTypeEnum.BASE64)
.pageToken("Y3Vyc29yX3Rva2VuX2V4YW1wbGU=")
.pageSize(50)
.build();
```

