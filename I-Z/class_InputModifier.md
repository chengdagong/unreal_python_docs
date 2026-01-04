# unreal.InputModifier

```python
class unreal.InputModifier(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


Base class for building modifiers.

**C++ Source:**

- **Plugin**: EnhancedInput

- **Module**: EnhancedInput

- **File**: InputModifiers.h



---

**get_visualization_color**( _sample_value_, _final_value_) → `LinearColor`

Helper to allow debug visualization of the modifier.

Parameters:

- **sample\_value** ( _InputActionValue_) – The base input action value pre-modification (ranging -1 -> 1 across all applicable axes).

- **final\_value** ( _InputActionValue_) – The post-modification input action value for the provided SampleValue.


Return type:

LinearColor


---

**modify_raw**( _player_input_, _current_value_, _delta_time_) → `InputActionValue`

ModifyRaw
Will be called by each modifier in the modifier chain

Parameters:

- **player\_input** ( _EnhancedPlayerInput_)

- **current\_value** ( _InputActionValue_) – The modified value returned by the previous modifier in the chain, or the base raw value if this is the first modifier in the chain.

- **delta\_time** ( _float_)


Return type:

InputActionValue

### Table of Contents

- `unreal.InputModifier`
  - `InputModifier`
    - `InputModifier.get_visualization_color()`
    - `InputModifier.modify_raw()`