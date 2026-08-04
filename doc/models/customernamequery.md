
# Customernamequery

## Structure

`Customernamequery`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CustomerName` | [`List<CustomerName>`](../../doc/models/customer-name.md) | Optional | **Constraints**: *Maximum Items*: `5` | List<CustomerName> getCustomerName() | setCustomerName(List<CustomerName> customerName) |

## Example

```java
import com.verizon.thingspace.models.CustomerName;
import com.verizon.thingspace.models.Customernamequery;
import java.util.Arrays;

Customernamequery customernamequery = new Customernamequery.Builder()
    .customerName(Arrays.asList(
        new CustomerName.Builder(
            "firstName4",
            "lastName4"
        )
        .title("title4")
        .middleName("middleName8")
        .suffix("suffix0")
        .build(),
        new CustomerName.Builder(
            "firstName4",
            "lastName4"
        )
        .title("title4")
        .middleName("middleName8")
        .suffix("suffix0")
        .build()
    ))
    .build();
```

