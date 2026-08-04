
# Asynchronous Location Request Result

## Structure

`AsynchronousLocationRequestResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Txid` | `String` | Optional | The transaction ID of the report. | String getTxid() | setTxid(String txid) |
| `Status` | [`ReportStatusEnum`](../../doc/models/report-status-enum.md) | Optional | Status of the report. | ReportStatusEnum getStatus() | setStatus(ReportStatusEnum status) |
| `EstimatedDuration` | `String` | Optional | Estimated number of minutes required to complete the report. | String getEstimatedDuration() | setEstimatedDuration(String estimatedDuration) |

## Example

```java
import com.verizon.thingspace.models.AsynchronousLocationRequestResult;
import com.verizon.thingspace.models.ReportStatusEnum;

AsynchronousLocationRequestResult asynchronousLocationRequestResult = new AsynchronousLocationRequestResult.Builder()
    .txid("2017-12-11Te8b47da2-eeee-ffff-gggg-61815e1e97e9")
    .status(ReportStatusEnum.QUEUED)
    .estimatedDuration("estimatedDuration6")
    .build();
```

