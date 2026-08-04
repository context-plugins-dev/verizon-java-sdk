
# Device List 2 Ids

## Class Name

`DeviceList2Ids`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`ESIMDeviceId`](../../../doc/models/esim-device-id.md) | DeviceList2Ids.fromESIMDeviceId(ESIMDeviceId eSIMDeviceId) |
| [`DeviceId2`](../../../doc/models/device-id-2.md) | DeviceList2Ids.fromDeviceId2(DeviceId2 deviceId2) |

## ESIMDeviceId

### Initialization Code

#### Example

```java
DeviceList2Ids.fromESIMDeviceId(
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
DeviceList2Ids.fromDeviceId2(
        new DeviceId2.Builder()
            .id("15-digit IMEI")
            .kind("imei")
            .build()
    )
```

