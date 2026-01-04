# unreal.AnimNotifyState

```python
class unreal.AnimNotifyState(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


Anim Notify State

**C++ Source:**

- **Module**: Engine

- **File**: AnimNotifyState.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `notify_color` (Color): [Read-Write] Color of Notify in editor

- `should_fire_in_editor` (bool): [Read-Write] Whether this notify state instance should fire in animation editors



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

**received_notify_begin**( _mesh_comp_, _animation_, _total_duration_, _event_reference_) → `bool`

Received Notify Begin

Parameters:

- **mesh\_comp** ( _SkeletalMeshComponent_)

- **animation** ( _AnimSequenceBase_)

- **total\_duration** ( _float_)

- **event\_reference** ( _AnimNotifyEventReference_)


Return type:

bool


---

**received_notify_end**( _mesh_comp_, _animation_, _event_reference_) → `bool`

Received Notify End

Parameters:

- **mesh\_comp** ( _SkeletalMeshComponent_)

- **animation** ( _AnimSequenceBase_)

- **event\_reference** ( _AnimNotifyEventReference_)


Return type:

bool


---

**received_notify_tick**( _mesh_comp_, _animation_, _frame_delta_time_, _event_reference_) → `bool`

Received Notify Tick

Parameters:

- **mesh\_comp** ( _SkeletalMeshComponent_)

- **animation** ( _AnimSequenceBase_)

- **frame\_delta\_time** ( _float_)

- **event\_reference** ( _AnimNotifyEventReference_)


Return type:

bool


---

_property_ `should_fire_in_editor`: bool

[Read-Only] Whether this notify state instance should fire in animation editors

**Type:**

( bool)

### Table of Contents

- `unreal.AnimNotifyState`
  - `AnimNotifyState`
    - `AnimNotifyState.get_default_trigger_weight_threshold()`
    - `AnimNotifyState.get_notify_name()`
    - `AnimNotifyState.notify_color`
    - `AnimNotifyState.received_notify_begin()`
    - `AnimNotifyState.received_notify_end()`
    - `AnimNotifyState.received_notify_tick()`
    - `AnimNotifyState.should_fire_in_editor`