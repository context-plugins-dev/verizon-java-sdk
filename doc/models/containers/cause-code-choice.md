
# Cause Code Choice

The main cause of a detected event. Each entry is of a different type and represents the sub cause code.

## Class Name

`CauseCodeChoice`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`TrafficConditionCauseCode`](../../../doc/models/traffic-condition-cause-code.md) | CauseCodeChoice.fromTrafficConditionCauseCode(TrafficConditionCauseCode trafficConditionCauseCode) |
| [`AccidentCauseCode`](../../../doc/models/accident-cause-code.md) | CauseCodeChoice.fromAccidentCauseCode(AccidentCauseCode accidentCauseCode) |
| [`RoadworksCauseCode`](../../../doc/models/roadworks-cause-code.md) | CauseCodeChoice.fromRoadworksCauseCode(RoadworksCauseCode roadworksCauseCode) |
| [`ImpassabilityCauseCode`](../../../doc/models/impassability-cause-code.md) | CauseCodeChoice.fromImpassabilityCauseCode(ImpassabilityCauseCode impassabilityCauseCode) |
| [`WrongWayDrivingCauseCode`](../../../doc/models/wrong-way-driving-cause-code.md) | CauseCodeChoice.fromWrongWayDrivingCauseCode(WrongWayDrivingCauseCode wrongWayDrivingCauseCode) |
| [`EmergencyVehicleApproachingCauseCode`](../../../doc/models/emergency-vehicle-approaching-cause-code.md) | CauseCodeChoice.fromEmergencyVehicleApproachingCauseCode(EmergencyVehicleApproachingCauseCode emergencyVehicleApproachingCauseCode) |

## TrafficConditionCauseCode

### Initialization Code

#### Example

```java
CauseCodeChoice.fromTrafficConditionCauseCode(
        new TrafficConditionCauseCode.Builder(
            26
        )
        .build()
    )
```

## AccidentCauseCode

### Initialization Code

#### Example

```java
CauseCodeChoice.fromAccidentCauseCode(
        new AccidentCauseCode.Builder(
            80
        )
        .build()
    )
```

## RoadworksCauseCode

### Initialization Code

#### Example

```java
CauseCodeChoice.fromRoadworksCauseCode(
        new RoadworksCauseCode.Builder(
            180
        )
        .build()
    )
```

## ImpassabilityCauseCode

### Initialization Code

#### Example

```java
CauseCodeChoice.fromImpassabilityCauseCode(
        new ImpassabilityCauseCode.Builder(
            80
        )
        .build()
    )
```

## WrongWayDrivingCauseCode

### Initialization Code

#### Example

```java
CauseCodeChoice.fromWrongWayDrivingCauseCode(
        new WrongWayDrivingCauseCode.Builder(
            172
        )
        .build()
    )
```

## EmergencyVehicleApproachingCauseCode

### Initialization Code

#### Example

```java
CauseCodeChoice.fromEmergencyVehicleApproachingCauseCode(
        new EmergencyVehicleApproachingCauseCode.Builder(
            88
        )
        .build()
    )
```

