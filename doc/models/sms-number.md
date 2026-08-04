
# SMS Number

Notification SMS details.

## Structure

`SMSNumber`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Carrier` | `String` | Optional | - | String getCarrier() | setCarrier(String carrier) |
| `Number` | `String` | Optional | - | String getNumber() | setNumber(String number) |

## Example

```java
import com.verizon.thingspace.models.SMSNumber;

SMSNumber sMSNumber = new SMSNumber.Builder()
    .carrier("US Cellular")
    .number("9299280711")
    .build();
```

