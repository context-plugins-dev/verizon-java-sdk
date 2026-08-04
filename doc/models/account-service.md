
# Account Service

Service associated with the account.

## Structure

`AccountService`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Optional | The name of the service plan. | String getName() | setName(String name) |
| `Description` | `String` | Optional | The description of the service plan. | String getDescription() | setDescription(String description) |
| `States` | [`List<State>`](../../doc/models/state.md) | Optional | The state of the service plan. | List<State> getStates() | setStates(List<State> states) |

## Example

```java
import com.verizon.thingspace.models.AccountService;
import com.verizon.thingspace.models.State;
import java.util.Arrays;

AccountService accountService = new AccountService.Builder()
    .name("Svc1")
    .description("Usage Segmentation - Main Line.")
    .states(Arrays.asList(
        new State.Builder()
            .name("Svc1 Activate")
            .workflowSequenceNumber(1D)
            .servicePlans(Arrays.asList(
                "4523aef7250f67205fd5",
                "4d4090c0f2d48814c94d"
            ))
            .build(),
        new State.Builder()
            .name("Svc1 No Telematics")
            .workflowSequenceNumber(3D)
            .servicePlans(Arrays.asList(
                "4523aef7250f67205fd5",
                "4d4090c0f2d48814c94d"
            ))
            .build(),
        new State.Builder()
            .name("Svc1 Deactivate")
            .workflowSequenceNumber(2D)
            .servicePlans(Arrays.asList(
                "4523aef7250f67205fd5",
                "4d4090c0f2d48814c94d"
            ))
            .build()
    ))
    .build();
```

