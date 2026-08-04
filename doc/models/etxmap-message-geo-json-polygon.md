
# ETXMAP Message Geo JSON Polygon

Query MAP records using a GeoJSON polygon to define the spatial area

## Structure

`ETXMAPMessageGeoJSONPolygon`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `MessageStandard` | [`ETXMessageStandardEnum`](../../doc/models/etx-message-standard-enum.md) | Optional | V2X messaging standard selection. Accepted values are 'sae' (SAE J2735) and 'etsi' (ETSI TS 103 301).<br><br>**Default**: `ETXMessageStandardEnum.SAE`<br><br>**Constraints**: *Maximum Length*: `4`, *Pattern*: `^(etsi\|sae)$` | ETXMessageStandardEnum getMessageStandard() | setMessageStandard(ETXMessageStandardEnum messageStandard) |
| `GeoJson` | `Object` | Required | GeoJSON Polygon defining the area to retrieve MAP messages for. | Object getGeoJson() | setGeoJson(Object geoJson) |
| `ExpectedType` | [`ETXExpectedTypeEnum`](../../doc/models/etx-expected-type-enum.md) | Optional | The format of the payload in the response body.<br><br>**Default**: `ETXExpectedTypeEnum.BASE64`<br><br>**Constraints**: *Maximum Length*: `6`, *Pattern*: `^(BASE64\|JSON)$` | ETXExpectedTypeEnum getExpectedType() | setExpectedType(ETXExpectedTypeEnum expectedType) |
| `PageToken` | `String` | Optional | Base64 encoded token used to retrieve the next page of results<br><br>**Constraints**: *Maximum Length*: `500`, *Pattern*: `^[A-Za-z0-9+/]+=*$` | String getPageToken() | setPageToken(String pageToken) |
| `PageSize` | `Integer` | Optional | Maximum number of records to return in a single page<br><br>**Default**: `200`<br><br>**Constraints**: `>= 1`, `<= 500` | Integer getPageSize() | setPageSize(Integer pageSize) |

## Example

```java
import com.verizon.thingspace.ApiHelper;
import com.verizon.thingspace.models.ETXExpectedTypeEnum;
import com.verizon.thingspace.models.ETXMAPMessageGeoJSONPolygon;
import com.verizon.thingspace.models.ETXMessageStandardEnum;
import java.io.IOException;

ETXMAPMessageGeoJSONPolygon eTXMAPMessageGeoJSONPolygon = new ETXMAPMessageGeoJSONPolygon.Builder(
    ApiHelper.deserialize("{\"type\":\"Polygon\",\"coordinates\":[[[-77.14,39.01],[-77.03,39.01],[-77.03,38.85],[-77.14,38.85],[-77.14,39.01]]]}")
)
.messageStandard(ETXMessageStandardEnum.SAE)
.expectedType(ETXExpectedTypeEnum.BASE64)
.pageToken("Y3Vyc29yX3Rva2VuX2V4YW1wbGU=")
.pageSize(50)
.build();
```

