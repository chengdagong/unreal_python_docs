# unreal.RigUnit_GetRelativeTransformForItem

```python
class unreal.RigUnit_GetRelativeTransformForItem(child:RigElementKey=Ellipsis, child_initial:bool=False, parent:RigElementKey=Ellipsis, parent_initial:bool=False, relative_transform:Transform=Ellipsis)
```


**Bases:** ``RigUnit``


GetRelativeTransform is used to retrieve a single transform from a hierarchy in the space of another transform

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_GetRelativeTransform.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `child` (RigElementKey): [Read-Write] The child item to retrieve the transform for

- `child_initial` (bool): [Read-Write] Defines if the child’s transform should be retrieved as current (false) or initial (true).
Initial transforms for bones and other elements in the hierarchy represent the reference pose’s value.

- `parent` (RigElementKey): [Read-Write] The parent item to use.
The child transform will be retrieve in the space of the parent.

- `parent_initial` (bool): [Read-Write] Defines if the parent’s transform should be retrieved as current (false) or initial (true).
Initial transforms for bones and other elements in the hierarchy represent the reference pose’s value.

- `relative_transform` (Transform): [Read-Write] The transform of the given child item relative to the provided parent



---

_property_ `child`: RigElementKey

[Read-Write] The child item to retrieve the transform for

**Type:**

( RigElementKey)


---

_property_ `child_initial`: bool

[Read-Write] Defines if the child’s transform should be retrieved as current (false) or initial (true).
Initial transforms for bones and other elements in the hierarchy represent the reference pose’s value.

**Type:**

( bool)


---

_property_ `parent`: RigElementKey

[Read-Write] The parent item to use.
The child transform will be retrieve in the space of the parent.

**Type:**

( RigElementKey)


---

_property_ `parent_initial`: bool

[Read-Write] Defines if the parent’s transform should be retrieved as current (false) or initial (true).
Initial transforms for bones and other elements in the hierarchy represent the reference pose’s value.

**Type:**

( bool)


---

_property_ `relative_transform`: Transform

[Read-Only] The transform of the given child item relative to the provided parent

**Type:**

( Transform)

### Table of Contents

- `unreal.RigUnit_GetRelativeTransformForItem`
  - `RigUnit_GetRelativeTransformForItem`
    - `RigUnit_GetRelativeTransformForItem.child`
    - `RigUnit_GetRelativeTransformForItem.child_initial`
    - `RigUnit_GetRelativeTransformForItem.parent`
    - `RigUnit_GetRelativeTransformForItem.parent_initial`
    - `RigUnit_GetRelativeTransformForItem.relative_transform`