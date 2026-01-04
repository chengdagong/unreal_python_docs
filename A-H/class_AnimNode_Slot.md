# unreal.AnimNode_Slot

```python
class unreal.AnimNode_Slot(source:PoseLink=\[\], slot_name:Name='None', always_update_source_pose:bool=False)
```


**Bases:** ``AnimNode_Base``


An animation slot node normally acts as a passthru, but a montage or PlaySlotAnimation call from
game code can cause an animation to blend in and be played on the slot temporarily, overriding the
Source input.

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_Slot.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `always_update_source_pose` (bool): [Read-Write] Whether we should continue to update the source pose regardless of whether it would be used.

- `slot_name` (Name): [Read-Write] The name of this slot, exposed to gameplay code, etc…

- `source` (PoseLink): [Read-Write] The source input, passed thru to the output unless a montage or slot animation is currently playing



---

_property_ `always_update_source_pose`: bool

[Read-Write] Whether we should continue to update the source pose regardless of whether it would be used.

**Type:**

( bool)


---

_property_ `slot_name`: Name

[Read-Write] The name of this slot, exposed to gameplay code, etc…

**Type:**

( Name)


---

_property_ `source`: PoseLink

[Read-Write] The source input, passed thru to the output unless a montage or slot animation is currently playing

**Type:**

( PoseLink)

### Table of Contents

- `unreal.AnimNode_Slot`
  - `AnimNode_Slot`
    - `AnimNode_Slot.always_update_source_pose`
    - `AnimNode_Slot.slot_name`
    - `AnimNode_Slot.source`