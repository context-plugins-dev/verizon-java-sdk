
# Description of Road Surface

Indicates the composition of the surface of the roadway for use in estimation of friction.

## Class Name

`DescriptionOfRoadSurface`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`DescriptionOfRoadSurfacePortlandCement`](../../../doc/models/description-of-road-surface-portland-cement.md) | DescriptionOfRoadSurface.fromDescriptionOfRoadSurfacePortlandCement(DescriptionOfRoadSurfacePortlandCement descriptionOfRoadSurfacePortlandCement) |
| [`DescriptionOfRoadSurfaceAsphaltOrTar`](../../../doc/models/description-of-road-surface-asphalt-or-tar.md) | DescriptionOfRoadSurface.fromDescriptionOfRoadSurfaceAsphaltOrTar(DescriptionOfRoadSurfaceAsphaltOrTar descriptionOfRoadSurfaceAsphaltOrTar) |
| [`DescriptionOfRoadSurfaceGravel`](../../../doc/models/description-of-road-surface-gravel.md) | DescriptionOfRoadSurface.fromDescriptionOfRoadSurfaceGravel(DescriptionOfRoadSurfaceGravel descriptionOfRoadSurfaceGravel) |
| [`DescriptionOfRoadSurfaceGrass`](../../../doc/models/description-of-road-surface-grass.md) | DescriptionOfRoadSurface.fromDescriptionOfRoadSurfaceGrass(DescriptionOfRoadSurfaceGrass descriptionOfRoadSurfaceGrass) |
| [`DescriptionOfRoadSurfaceCinders`](../../../doc/models/description-of-road-surface-cinders.md) | DescriptionOfRoadSurface.fromDescriptionOfRoadSurfaceCinders(DescriptionOfRoadSurfaceCinders descriptionOfRoadSurfaceCinders) |
| [`DescriptionOfRoadSurfaceRock`](../../../doc/models/description-of-road-surface-rock.md) | DescriptionOfRoadSurface.fromDescriptionOfRoadSurfaceRock(DescriptionOfRoadSurfaceRock descriptionOfRoadSurfaceRock) |
| [`DescriptionOfRoadSurfaceIce`](../../../doc/models/description-of-road-surface-ice.md) | DescriptionOfRoadSurface.fromDescriptionOfRoadSurfaceIce(DescriptionOfRoadSurfaceIce descriptionOfRoadSurfaceIce) |
| [`DescriptionOfRoadSurfaceSnow`](../../../doc/models/description-of-road-surface-snow.md) | DescriptionOfRoadSurface.fromDescriptionOfRoadSurfaceSnow(DescriptionOfRoadSurfaceSnow descriptionOfRoadSurfaceSnow) |

## DescriptionOfRoadSurfacePortlandCement

### Initialization Code

#### Example

```java
DescriptionOfRoadSurface.fromDescriptionOfRoadSurfacePortlandCement(
        new DescriptionOfRoadSurfacePortlandCement.Builder(
            new PortlandCement.Builder()
                .type(Type6Enum.TRAVELED)
                .build()
        )
        .build()
    )
```

## DescriptionOfRoadSurfaceAsphaltOrTar

### Initialization Code

#### Example

```java
DescriptionOfRoadSurface.fromDescriptionOfRoadSurfaceAsphaltOrTar(
        new DescriptionOfRoadSurfaceAsphaltOrTar.Builder(
            new AsphaltOrTar.Builder()
                .build()
        )
        .build()
    )
```

## DescriptionOfRoadSurfaceGravel

### Initialization Code

#### Example

```java
DescriptionOfRoadSurface.fromDescriptionOfRoadSurfaceGravel(
        new DescriptionOfRoadSurfaceGravel.Builder(
            new Gravel.Builder()
                .build()
        )
        .build()
    )
```

## DescriptionOfRoadSurfaceGrass

### Initialization Code

#### Example

```java
DescriptionOfRoadSurface.fromDescriptionOfRoadSurfaceGrass(
        new DescriptionOfRoadSurfaceGrass.Builder(
            new Grass.Builder()
                .build()
        )
        .build()
    )
```

## DescriptionOfRoadSurfaceCinders

### Initialization Code

#### Example

```java
DescriptionOfRoadSurface.fromDescriptionOfRoadSurfaceCinders(
        new DescriptionOfRoadSurfaceCinders.Builder(
            new Cinders.Builder()
                .build()
        )
        .build()
    )
```

## DescriptionOfRoadSurfaceRock

### Initialization Code

#### Example

```java
DescriptionOfRoadSurface.fromDescriptionOfRoadSurfaceRock(
        new DescriptionOfRoadSurfaceRock.Builder(
            new Rock.Builder()
                .build()
        )
        .build()
    )
```

## DescriptionOfRoadSurfaceIce

### Initialization Code

#### Example

```java
DescriptionOfRoadSurface.fromDescriptionOfRoadSurfaceIce(
        new DescriptionOfRoadSurfaceIce.Builder(
            new Ice.Builder()
                .build()
        )
        .build()
    )
```

## DescriptionOfRoadSurfaceSnow

### Initialization Code

#### Example

```java
DescriptionOfRoadSurface.fromDescriptionOfRoadSurfaceSnow(
        new DescriptionOfRoadSurfaceSnow.Builder(
            new Snow.Builder()
                .build()
        )
        .build()
    )
```

