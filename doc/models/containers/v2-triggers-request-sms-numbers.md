
# V2 Triggers Request Sms Numbers

## Class Name

`V2TriggersRequestSmsNumbers`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`Cellphonenumber`](../../../doc/models/cellphonenumber.md) | V2TriggersRequestSmsNumbers.fromCellphonenumber(Cellphonenumber cellphonenumber) |

## Cellphonenumber

### Initialization Code

#### Example

```java
V2TriggersRequestSmsNumbers.fromCellphonenumber(
        new Cellphonenumber.Builder()
            .number("10-digit mobile number")
            .carrier("mobile service provider")
            .build()
    )
```

