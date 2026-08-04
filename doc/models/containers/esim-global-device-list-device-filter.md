
# ESIM Global Device List Device Filter

## Class Name

`ESIMGlobalDeviceListDeviceFilter`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`ESIMDeviceId`](../../../doc/models/esim-device-id.md) | ESIMGlobalDeviceListDeviceFilter.fromESIMDeviceId(ESIMDeviceId eSIMDeviceId) |
| [`DeviceId2`](../../../doc/models/device-id-2.md) | ESIMGlobalDeviceListDeviceFilter.fromDeviceId2(DeviceId2 deviceId2) |

## ESIMDeviceId

### Initialization Code

#### Example

```java
ESIMGlobalDeviceListDeviceFilter.fromESIMDeviceId(
        new ESIMDeviceId.Builder()
            .id("32-digit EID")
            .kind("eid")
            .build()
    )
```

## DeviceId2

### Initialization Code

#### Example

```java
ESIMGlobalDeviceListDeviceFilter.fromDeviceId2(
        new DeviceId2.Builder()
            .id("15-digit IMEI")
            .kind("imei")
            .build()
    )
```

