
# Security Subscription Result

Response for a subscription request.

## Structure

`SecuritySubscriptionResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Optional | The name of a billing account. | String getAccountName() | setAccountName(String accountName) |
| `SubscriptionList` | [`List<SecuritySubscription>`](../../doc/models/security-subscription.md) | Optional | The list of SKU numbers and counts for each license type specified in the request.<br><br>**Constraints**: *Maximum Items*: `5` | List<SecuritySubscription> getSubscriptionList() | setSubscriptionList(List<SecuritySubscription> subscriptionList) |

## Example

```java
import com.verizon.thingspace.models.ExtendedAttributes;
import com.verizon.thingspace.models.SecuritySubscription;
import com.verizon.thingspace.models.SecuritySubscriptionResult;
import java.util.Arrays;

SecuritySubscriptionResult securitySubscriptionResult = new SecuritySubscriptionResult.Builder()
    .accountName("000012345600001")
    .subscriptionList(Arrays.asList(
        new SecuritySubscription.Builder()
            .extendedAttributes(Arrays.asList(
                new ExtendedAttributes.Builder()
                    .key("key8")
                    .value("value0")
                    .build(),
                new ExtendedAttributes.Builder()
                    .key("key8")
                    .value("value0")
                    .build()
            ))
            .licenseAssigned(7)
            .licenseAvailable(1)
            .licensePurchased(9)
            .licenseType("Flexible Bundle")
            .skuNumber("TS-BUNDLE-KTO-SIMSEC-MRC")
            .build()
    ))
    .build();
```

