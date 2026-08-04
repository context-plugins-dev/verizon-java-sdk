
# M5 G Bichange Request Device List with Service Address

## Class Name

`M5gBichangeRequestDeviceListWithServiceAddress`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`M5gBideviceIdarray2`](../../../doc/models/m5-g-bidevice-idarray-2.md) | M5gBichangeRequestDeviceListWithServiceAddress.fromM5gBideviceIdarray2(M5gBideviceIdarray2 m5gBideviceIdarray2) |
| [`M5gBiaddressAndcustomerinfo2`](../../../doc/models/m5-g-biaddress-andcustomerinfo-2.md) | M5gBichangeRequestDeviceListWithServiceAddress.fromM5gBiaddressAndcustomerinfo2(M5gBiaddressAndcustomerinfo2 m5gBiaddressAndcustomerinfo2) |

## M5gBideviceIdarray2

### Initialization Code

#### Example

```java
M5gBichangeRequestDeviceListWithServiceAddress.fromM5gBideviceIdarray2(
        new M5gBideviceIdarray2.Builder()
            .build()
    )
```

## M5gBiaddressAndcustomerinfo2

### Initialization Code

#### Example

```java
M5gBichangeRequestDeviceListWithServiceAddress.fromM5gBiaddressAndcustomerinfo2(
        new M5gBiaddressAndcustomerinfo2.Builder()
            .primaryPlaceofuse(new M5gBiaddressAndcustomerinfo.Builder()
                .build())
            .build()
    )
```

