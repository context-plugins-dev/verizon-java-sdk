
# ETXMAP Data Ingest Request

JSON representation of a J2735/ETSI MapData message for ingestion. The value field must contain a valid MAP message body conforming to the SAE J2735 or ETSI TS 103 301 standard.

## Structure

`ETXMAPDataIngestRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `MessageId` | `int` | Required | SAE J2735 DSRCmsgID for the MAP message type.<br><br>**Constraints**: `>= 0`, `<= 32767` | int getMessageId() | setMessageId(int messageId) |
| `Value` | `Object` | Required | The decoded MAP message body containing intersection and lane data. | Object getValue() | setValue(Object value) |
| `MsgIssueRevision` | `Integer` | Optional | Issue revision number of the MAP message.<br><br>**Constraints**: `>= 0`, `<= 255` | Integer getMsgIssueRevision() | setMsgIssueRevision(Integer msgIssueRevision) |

## Example

```java
import com.verizon.thingspace.ApiHelper;
import com.verizon.thingspace.models.ETXMAPDataIngestRequest;
import java.io.IOException;

ETXMAPDataIngestRequest eTXMAPDataIngestRequest = new ETXMAPDataIngestRequest.Builder(
    18,
    ApiHelper.deserialize("{\"intersections\":[{\"id\":{\"region\":0,\"id\":156},\"laneWidth\":366,\"refPoint\":{\"lat\":389284111,\"long\":-772410713},\"revision\":3}],\"msgIssueRevision\":3}")
)
.msgIssueRevision(50)
.build();
```

