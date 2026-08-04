
# Deactivate Device List Ids

## Class Name

`DeactivateDeviceListIds`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`DeviceId`](../../../doc/models/device-id.md) | DeactivateDeviceListIds.fromDeviceId(DeviceId deviceId) |
| [`PropertyDeviceId`](../../../doc/models/property-device-id.md) | DeactivateDeviceListIds.fromPropertyDeviceId(PropertyDeviceId propertyDeviceId) |

## DeviceId

### Initialization Code

#### Example

```java
DeactivateDeviceListIds.fromDeviceId(
        new DeviceId.Builder(
            "990013907835573",
            "imei"
        )
        .build()
    )
```

## PropertyDeviceId

### Initialization Code

#### Example

```java
DeactivateDeviceListIds.fromPropertyDeviceId(
        new PropertyDeviceId.Builder()
            .kind("imei")
            .build()
    )
```

