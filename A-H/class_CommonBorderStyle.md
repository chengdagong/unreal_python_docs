# unreal.CommonBorderStyle

```python
class unreal.CommonBorderStyle(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


- —\- All properties must be EditDefaultsOnly, BlueprintReadOnly !!! —–

- We return the CDO to blueprints, so we cannot allow any changes (blueprint doesn’t support const variables)


**C++ Source:**

- **Plugin**: CommonUI

- **Module**: CommonUI

- **File**: CommonBorder.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `background` (SlateBrush): [Read-Write] The brush for the background of the border



---

_property_ `background`: SlateBrush

[Read-Only] The brush for the background of the border

**Type:**

( SlateBrush)


---

**get_background_brush**() → `SlateBrush`

Get Background Brush

Returns:

brush (SlateBrush):

Return type:

SlateBrush

### Table of Contents

- `unreal.CommonBorderStyle`
  - `CommonBorderStyle`
    - `CommonBorderStyle.background`
    - `CommonBorderStyle.get_background_brush()`