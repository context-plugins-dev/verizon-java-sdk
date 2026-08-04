
# Cellphonenumber

## Structure

`Cellphonenumber`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Number` | `String` | Optional | - | String getNumber() | setNumber(String number) |
| `Carrier` | `String` | Optional | - | String getCarrier() | setCarrier(String carrier) |

## Example

```java
import com.verizon.thingspace.models.Cellphonenumber;

Cellphonenumber cellphonenumber = new Cellphonenumber.Builder()
    .number("10-digit mobile number")
    .carrier("mobile service provider")
    .build();
```

