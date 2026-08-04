
# V2 Triggers Request 1 Sms Numbers

## Class Name

`V2TriggersRequest1SmsNumbers`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`Cellphonenumber`](../../../doc/models/cellphonenumber.md) | V2TriggersRequest1SmsNumbers.fromCellphonenumber(Cellphonenumber cellphonenumber) |

## Cellphonenumber

### Initialization Code

#### Example

```java
V2TriggersRequest1SmsNumbers.fromCellphonenumber(
        new Cellphonenumber.Builder()
            .number("10-digit mobile number")
            .carrier("mobile service provider")
            .build()
    )
```

