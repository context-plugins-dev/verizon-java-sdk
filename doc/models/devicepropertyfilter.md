
# Devicepropertyfilter

## Structure

`Devicepropertyfilter`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Selection` | [`Devicepropertyselection`](../../doc/models/devicepropertyselection.md) | Optional | - | Devicepropertyselection getSelection() | setSelection(Devicepropertyselection selection) |
| `Querytotalcount` | `Boolean` | Optional | - | Boolean getQuerytotalcount() | setQuerytotalcount(Boolean querytotalcount) |

## Example

```java
import com.verizon.thingspace.models.Devicepropertyfilter;
import com.verizon.thingspace.models.Devicepropertyselection;

Devicepropertyfilter devicepropertyfilter = new Devicepropertyfilter.Builder()
    .selection(new Devicepropertyselection.Builder()
        .modelid("modelid0")
        .build())
    .querytotalcount(true)
    .build();
```

