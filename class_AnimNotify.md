# unreal.AnimNotify

```python
class unreal.AnimNotify(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


Anim Notify

**C++ Source:**

- **Module**: Engine

- **File**: AnimNotify.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `notify_color` (Color): [Read-Write] Color of Notify in editor

- `should_fire_in_editor` (bool): [Read-Write] Whether this notify instance should fire in animation editors



---

**get_default_trigger_weight_threshold**() → `float`

TriggerWeightThreshold to use when creating notifies of this type

Return type:

float


---

**get_notify_name**() → `str`

Implementable event to get a custom name for the notify

Return type:

str


---

_property_ `notify_color`: Color

[Read-Only] Color of Notify in editor

**Type:**

( Color)


---

**received_notify**( _mesh_comp_, _animation_, _event_reference_) → `bool`

Received Notify

Parameters:

- **mesh\_comp** ( _SkeletalMeshComponent_)

- **animation** ( _AnimSequenceBase_)

- **event\_reference** ( _AnimNotifyEventReference_)


Return type:

bool


---

_property_ `should_fire_in_editor`: bool

[Read-Only] Whether this notify instance should fire in animation editors

**Type:**

( bool)

### Table of Contents

- `unreal.AnimNotify`
  - `AnimNotify`
    - `AnimNotify.get_default_trigger_weight_threshold()`
    - `AnimNotify.get_notify_name()`
    - `AnimNotify.notify_color`
    - `AnimNotify.received_notify()`
    - `AnimNotify.should_fire_in_editor`