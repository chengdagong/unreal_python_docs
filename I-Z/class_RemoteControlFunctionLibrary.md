# unreal.RemoteControlFunctionLibrary

```python
class unreal.RemoteControlFunctionLibrary(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


Remote Control Function Library

**C++ Source:**

- **Plugin**: RemoteControl

- **Module**: RemoteControl

- **File**: RemoteControlFunctionLibrary.h



---

_classmethod_ apply_color_grading_wheel_delta( _target_object_, _property_name_, _delta_value_, _reference_color_, _is_interactive_, _min_value=0.000000_, _max_value=2.000000_)→bool

Add/subtract from the value of an FVector4 property interpreted as RGBV using a delta value based on color wheel coordinates.

Parameters:

- **target\_object** ( _Object_) – the object that contains the property to modify.

- **property\_name** ( _str_) – the name of the property to modify.

- **delta\_value** ( _ColorGradingWheelColor_) – the amount to change the color by.

- **reference\_color** ( _ColorGradingWheelColor_) – if the color’s current position on the wheel is ambiguous as calculated from RGB values (e.g. black), use this reference color’s position instead.

- **is\_interactive** ( _bool_) – if true, this is treated as an interactive change. If false, it will be treated as the final value set change.

- **min\_value** ( _float_)

- **max\_value** ( _float_)


Returns:

Whether the operation was successful.

Return type:

bool


---

_classmethod_ apply_color_wheel_delta( _target_object_, _property_name_, _delta_value_, _reference_color_, _is_interactive_)→bool

Add/subtract from the value of an FLinearColor property using a delta value based on color wheel coordinates.

Parameters:

- **target\_object** ( _Object_) – the object that contains the property to modify.

- **property\_name** ( _str_) – the name of the property to modify.

- **delta\_value** ( _ColorWheelColor_) – the amount to change the color by.

- **reference\_color** ( _ColorWheelColor_) – if the color’s current position on the wheel is ambiguous as calculated from RGB values (e.g. black), use this reference color’s position instead.

- **is\_interactive** ( _bool_) – if true, this is treated as an interactive change. If false, it will be treated as the final value set change.


Returns:

Whether the operation was successful.

Return type:

bool


---

_classmethod_ expose_actor( _preset_, _actor_, _args_)→bool

Expose an actor in a remote control preset.

Parameters:

- **preset** ( _RemoteControlPreset_) – the preset to expose the property in.

- **actor** ( _Actor_) – the actor to expose.

- **args** ( _RemoteControlOptionalExposeArgs_) – optional arguments.


Returns:

Whether the operation was successful.

Return type:

bool


---

_classmethod_ expose_function( _preset_, _source_object_, _function_, _args_)→bool

Expose a function in a remote control preset.

Parameters:

- **preset** ( _RemoteControlPreset_) – the preset to expose the property in.

- **source\_object** ( _Object_) – the object that contains the property to expose.

- **function** ( _str_) – the name of the function to expose.

- **args** ( _RemoteControlOptionalExposeArgs_) – optional arguments.


Returns:

Whether the operation was successful.

Return type:

bool


---

_classmethod_ expose_property( _preset_, _source_object_, _property__, _args_)→bool

Expose a property in a remote control preset.

Parameters:

- **preset** ( _RemoteControlPreset_) – the preset to expose the property in.

- **source\_object** ( _Object_) – the object that contains the property to expose.

- **property** ( _str_) – the name or path of the property to expose.

- **args** ( _RemoteControlOptionalExposeArgs_) – optional arguments.


Returns:

Whether the operation was successful.

Return type:

bool

### Table of Contents

- `unreal.RemoteControlFunctionLibrary`
  - `RemoteControlFunctionLibrary`
    - `RemoteControlFunctionLibrary.apply_color_grading_wheel_delta()`
    - `RemoteControlFunctionLibrary.apply_color_wheel_delta()`
    - `RemoteControlFunctionLibrary.expose_actor()`
    - `RemoteControlFunctionLibrary.expose_function()`
    - `RemoteControlFunctionLibrary.expose_property()`