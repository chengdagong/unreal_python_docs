# unreal.MetaHumanCharacterInstanceParameter

```python
class unreal.MetaHumanCharacterInstanceParameter(name:Name='None', type:MetaHumanCharacterInstanceParameterType=0, item_path:MetaHumanPaletteItemPath=\[\])
```


**Bases:** ``StructBase``


brief: Struct that represents a parameter of a particular item in a collection This struct is designed to work in scripting environments and will have functions to get and set values hoisted from UMetaHumanCharacterInstanceParameterBlueprintLibrary Note that calling one of the Set functions automatically update the parameter value for the item it represents in the instance that was used when querying them.

**C++ Source:**

- **Plugin**: MetaHumanCharacter

- **Module**: MetaHumanCharacterPaletteEditor

- **File**: MetaHumanCollectionBlueprintLibrary.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `item_path` (MetaHumanPaletteItemPath): [Read-Only] The item path to locate this parameter in the instance

- `name` (Name): [Read-Only] The name of the parameter

- `type` (MetaHumanCharacterInstanceParameterType): [Read-Only] The type of the parameter. Can be used to check which of Set/Get functions to call



---

**get_bool**() → `boolorNone`

Get Bool

Returns:

out\_value (bool):

Return type:

bool or None


---

**get_color**() → `LinearColororNone`

Get Color

Returns:

out\_value (LinearColor):

Return type:

LinearColor or None


---

**get_float**() → `floatorNone`

Get Float

Returns:

out\_value (float):

Return type:

float or None


---

_property_ `item_path`: MetaHumanPaletteItemPath

[Read-Only] The item path to locate this parameter in the instance

**Type:**

( MetaHumanPaletteItemPath)


---

_property_ `name`: Name

[Read-Only] The name of the parameter

**Type:**

( Name)


---

**set_bool**( _value_) → `bool`

Set Bool

Parameters:

**value** ( _bool_)

Return type:

bool


---

**set_color**( _value_) → `bool`

Set Color

Parameters:

**value** ( _LinearColor_)

Return type:

bool


---

**set_float**( _value_) → `bool`

Set Float

Parameters:

**value** ( _float_)

Return type:

bool


---

_property_ `type`: MetaHumanCharacterInstanceParameterType

[Read-Only] The type of the parameter. Can be used to check which of Set/Get functions to call

**Type:**

( MetaHumanCharacterInstanceParameterType)

### Table of Contents

- `unreal.MetaHumanCharacterInstanceParameter`
  - `MetaHumanCharacterInstanceParameter`
    - `MetaHumanCharacterInstanceParameter.get_bool()`
    - `MetaHumanCharacterInstanceParameter.get_color()`
    - `MetaHumanCharacterInstanceParameter.get_float()`
    - `MetaHumanCharacterInstanceParameter.item_path`
    - `MetaHumanCharacterInstanceParameter.name`
    - `MetaHumanCharacterInstanceParameter.set_bool()`
    - `MetaHumanCharacterInstanceParameter.set_color()`
    - `MetaHumanCharacterInstanceParameter.set_float()`
    - `MetaHumanCharacterInstanceParameter.type`