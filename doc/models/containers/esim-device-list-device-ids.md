
# ESIM Device List Device Ids

## Class Name

`ESIMDeviceListDeviceIds`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`ESIMDeviceId`](../../../doc/models/esim-device-id.md) | ESIMDeviceListDeviceIds.fromESIMDeviceId(ESIMDeviceId eSIMDeviceId) |
| [`DeviceId2`](../../../doc/models/device-id-2.md) | ESIMDeviceListDeviceIds.fromDeviceId2(DeviceId2 deviceId2) |

## ESIMDeviceId

### Initialization Code

#### Example

```java
ESIMDeviceListDeviceIds.fromESIMDeviceId(
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
ESIMDeviceListDeviceIds.fromDeviceId2(
        new DeviceId2.Builder()
            .id("15-digit IMEI")
            .kind("imei")
            .build()
    )
```

