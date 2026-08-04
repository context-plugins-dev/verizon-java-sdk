
# Status Response

## Structure

`StatusResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `RequestId` | `String` | Optional | **Constraints**: *Minimum Length*: `3`, *Maximum Length*: `64`, *Pattern*: `^[a-z-0-9]{3,64}$` | String getRequestId() | setRequestId(String requestId) |
| `Status` | `String` | Optional | **Constraints**: *Minimum Length*: `3`, *Maximum Length*: `32`, *Pattern*: `^[A-Za-z0-9]{3,32}$` | String getStatus() | setStatus(String status) |
| `Subrequests` | [`List<Subrequest>`](../../doc/models/subrequest.md) | Optional | **Constraints**: *Maximum Items*: `100` | List<Subrequest> getSubrequests() | setSubrequests(List<Subrequest> subrequests) |

## Example

```java
import com.verizon.thingspace.models.GIODeviceId;
import com.verizon.thingspace.models.StatusResponse;
import com.verizon.thingspace.models.Subrequest;
import java.util.Arrays;

StatusResponse statusResponse = new StatusResponse.Builder()
    .requestId("d1f08526-5443-4054-9a29-4456490ea9f8")
    .status("Success")
    .subrequests(Arrays.asList(
        new Subrequest.Builder()
            .ids(new GIODeviceId.Builder(
                "kind2",
                "id4"
            )
            .build())
            .status("status2")
            .build(),
        new Subrequest.Builder()
            .ids(new GIODeviceId.Builder(
                "kind2",
                "id4"
            )
            .build())
            .status("status2")
            .build()
    ))
    .build();
```

