
# Domestic 4 G and 5G Nationwide Network Coverage Body

## Class Name

`Domestic4GAnd5gNationwideNetworkCoverageBody`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`GetWirelessCoverageRequest`](../../../doc/models/get-wireless-coverage-request.md) | Domestic4GAnd5gNationwideNetworkCoverageBody.fromGetWirelessCoverageRequest(GetWirelessCoverageRequest getWirelessCoverageRequest) |
| [`GetWirelessCoverageRequestFWA`](../../../doc/models/get-wireless-coverage-request-fwa.md) | Domestic4GAnd5gNationwideNetworkCoverageBody.fromGetWirelessCoverageRequestFWA(GetWirelessCoverageRequestFWA getWirelessCoverageRequestFWA) |

## GetWirelessCoverageRequest

### Initialization Code

#### Example

```java
Domestic4GAnd5gNationwideNetworkCoverageBody.fromGetWirelessCoverageRequest(
        new GetWirelessCoverageRequest.Builder(
            "0000123456-00001",
            "NW",
            "LONGLAT",
            new Locationscoord.Builder()
                .build(),
            Arrays.asList(
                new NetworkTypeObject.Builder()
                    .networkType("LTE")
                    .build()
            )
        )
        .build()
    )
```

## GetWirelessCoverageRequestFWA

### Initialization Code

#### Example

```java
Domestic4GAnd5gNationwideNetworkCoverageBody.fromGetWirelessCoverageRequestFWA(
        new GetWirelessCoverageRequestFWA.Builder(
            "0000123456-00001",
            "NW",
            "ADDRESS",
            new Locations.Builder()
                .build(),
            Arrays.asList(
                new NetworkTypeObject.Builder()
                    .networkType("LTE")
                    .build()
            )
        )
        .build()
    )
```

