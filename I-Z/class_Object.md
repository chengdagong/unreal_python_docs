# unreal.Object

```python
class unreal.Object(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``_ObjectBase``


The base class of all UE objects. The type of an object is defined by its UClass.
This provides support functions for creating and using objects, and virtual functions that should be overridden in child classes.
see: https://docs.unrealengine.com/ProgrammingAndScripting/ProgrammingWithCPP/UnrealArchitecture/Objects

**C++ Source:**

- **Module**: CoreUObject

- **File**: Object.h



---

**acquire_editor_element_handle**( _allow_create=True_) → `ScriptTypedElementHandle`

K2 Acquire Editor Object Element Handle

Parameters:

**allow\_create** ( _bool_)

Return type:

ScriptTypedElementHandle


---

**is_editor_property_overridden**( _property_name_) → `EditorPropertyValueState`

Attempts to query whether the value of a named property on the given object overrides the value of its archetype (ie, would ResetEditorProperty do anything?).

Parameters:

**property\_name** ( _Name_) – The name of the object property to query the value of.

Returns:

What state the requested property is in.

Return type:

EditorPropertyValueState


---

**reset_editor_property**( _property_name_, _change_notify_mode=PropertyAccessChangeNotifyMode.DEFAULT_) → `bool`

Attempts to reset the value of a named property on the given object so that it matches the value of the archetype.

Parameters:

- **property\_name** ( _Name_) – The name of the object property to reset the value of.

- **change\_notify\_mode** ( _PropertyAccessChangeNotifyMode_) – When to emit property change notifications.


Returns:

Whether the property value was found and correctly reset.

Return type:

bool

### Table of Contents

- `unreal.Object`
  - `Object`
    - `Object.acquire_editor_element_handle()`
    - `Object.is_editor_property_overridden()`
    - `Object.reset_editor_property()`