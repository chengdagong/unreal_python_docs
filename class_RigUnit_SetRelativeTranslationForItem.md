# unreal.RigUnit_SetRelativeTranslationForItem

```python
class unreal.RigUnit_SetRelativeTranslationForItem(execute_pin:RigVMExecutePin=\[\], child:RigElementKey=Ellipsis, parent:RigElementKey=Ellipsis, parent_initial:bool=False, value:Vector=Ellipsis, weight:float=0.0, propagate_to_children:bool=False)
```


**Bases:** ``RigUnitMutable``


SetRelativeTranslation is used to set a single translation from a hierarchy in the space of another item

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_SetRelativeTransform.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `child` (RigElementKey): [Read-Write] The child item to set the transform for

- `execute_pin` (RigVMExecutePin): [Read-Write] \* This property is used to chain multiple mutable units together

- `parent` (RigElementKey): [Read-Write] The parent item to use.
The child transform will be set in the space of the parent.

- `parent_initial` (bool): [Read-Write] Defines if the parent’s transform should be determined as current (false) or initial (true).
Initial transforms for bones and other elements in the hierarchy represent the reference pose’s value.

- `propagate_to_children` (bool): [Read-Write] If set to true children of affected items in the hierarchy
will follow the transform change - otherwise only the parent will move.

- `value` (Vector): [Read-Write] The transform of the child item relative to the provided parent

- `weight` (float): [Read-Write] Defines how much the change will be applied



---

_property_ `child`: RigElementKey

[Read-Write] The child item to set the transform for

**Type:**

( RigElementKey)


---

_property_ `parent`: RigElementKey

[Read-Write] The parent item to use.
The child transform will be set in the space of the parent.

**Type:**

( RigElementKey)


---

_property_ `parent_initial`: bool

[Read-Write] Defines if the parent’s transform should be determined as current (false) or initial (true).
Initial transforms for bones and other elements in the hierarchy represent the reference pose’s value.

**Type:**

( bool)


---

_property_ `propagate_to_children`: bool

[Read-Write] If set to true children of affected items in the hierarchy
will follow the transform change - otherwise only the parent will move.

**Type:**

( bool)


---

_property_ `value`: Vector

[Read-Write] The transform of the child item relative to the provided parent

**Type:**

( Vector)


---

_property_ `weight`: float

[Read-Write] Defines how much the change will be applied

**Type:**

( float)

### Table of Contents

- `unreal.RigUnit_SetRelativeTranslationForItem`
  - `RigUnit_SetRelativeTranslationForItem`
    - `RigUnit_SetRelativeTranslationForItem.child`
    - `RigUnit_SetRelativeTranslationForItem.parent`
    - `RigUnit_SetRelativeTranslationForItem.parent_initial`
    - `RigUnit_SetRelativeTranslationForItem.propagate_to_children`
    - `RigUnit_SetRelativeTranslationForItem.value`
    - `RigUnit_SetRelativeTranslationForItem.weight`