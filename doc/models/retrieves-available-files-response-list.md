
# Retrieves Available Files Response List

## Structure

`RetrievesAvailableFilesResponseList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AvailableFilesResponse` | [`List<RetrievesAvailableFilesResponse>`](../../doc/models/retrieves-available-files-response.md) | Optional | **Constraints**: *Maximum Items*: `100` | List<RetrievesAvailableFilesResponse> getAvailableFilesResponse() | setAvailableFilesResponse(List<RetrievesAvailableFilesResponse> availableFilesResponse) |

## Example

```java
import com.verizon.thingspace.models.RetrievesAvailableFilesResponse;
import com.verizon.thingspace.models.RetrievesAvailableFilesResponseList;
import java.util.Arrays;

RetrievesAvailableFilesResponseList retrievesAvailableFilesResponseList = new RetrievesAvailableFilesResponseList.Builder()
    .availableFilesResponse(Arrays.asList(
        new RetrievesAvailableFilesResponse.Builder()
            .fileName("fileName2")
            .fileVersion("fileVersion4")
            .releaseNote("releaseNote0")
            .make("make2")
            .model("model6")
            .build()
    ))
    .build();
```

