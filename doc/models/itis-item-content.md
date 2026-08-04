
# ITIS Item Content

An item object wrapping an ITIS code value.

## Structure

`ITISItemContent`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Itis` | `int` | Required | The ITIS Code that describes the alert/danger/hazard. All ITS standards use the same types here to explain the type of the alert/danger/hazard involved.<br><br>The complete set of ITIS codes can be found in Volume Two of the SAE J2540 standard. This is a set of over 1000 items which are used to encode common events and list items in ITS.<br><br>**Constraints**: `>= 0`, `<= 65535` | int getItis() | setItis(int itis) |

## Example

```java
import com.verizon.thingspace.models.ITISItemContent;

ITISItemContent iTISItemContent = new ITISItemContent.Builder(
    202
)
.build();
```

