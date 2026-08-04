
# Engagement

The engagements associated with the account.

## Structure

`Engagement`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `EngagementId` | `String` | Optional | The engagement ID. | String getEngagementId() | setEngagementId(String engagementId) |
| `ChargingGroup` | `String` | Optional | The charging group name. | String getChargingGroup() | setChargingGroup(String chargingGroup) |
| `Services` | [`List<AccountService>`](../../doc/models/account-service.md) | Optional | The services associated with the account. | List<AccountService> getServices() | setServices(List<AccountService> services) |

## Example

```java
import com.verizon.thingspace.models.AccountService;
import com.verizon.thingspace.models.Engagement;
import com.verizon.thingspace.models.State;
import java.util.Arrays;

Engagement engagement = new Engagement.Builder()
    .engagementId("1234")
    .chargingGroup("Engagement1234")
    .services(Arrays.asList(
        new AccountService.Builder()
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
            .build(),
        new AccountService.Builder()
            .name("WIFI")
            .description("Usage Segmentation - WiFi.")
            .states(Arrays.asList(
                new State.Builder()
                    .name("WIFI Redirect")
                    .workflowSequenceNumber(2D)
                    .servicePlans(Arrays.asList(
                        "4d4090c0f2d48814c94d"
                    ))
                    .build(),
                new State.Builder()
                    .name("WIFI Trial")
                    .workflowSequenceNumber(4D)
                    .servicePlans(Arrays.asList(
                        "4d4090c0f2d48814c94d"
                    ))
                    .build(),
                new State.Builder()
                    .name("WIFI Goodwill")
                    .workflowSequenceNumber(6D)
                    .servicePlans(Arrays.asList(
                        "4d4090c0f2d48814c94d"
                    ))
                    .build(),
                new State.Builder()
                    .name("WIFI Disable")
                    .workflowSequenceNumber(3D)
                    .servicePlans(Arrays.asList(
                        "4d4090c0f2d48814c94d"
                    ))
                    .build()
            ))
            .build()
    ))
    .build();
```

