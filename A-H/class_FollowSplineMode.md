# unreal.FollowSplineMode

```python
class unreal.FollowSplineMode(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BaseMovementMode``


FollowSplineMode: This mode performs movement of the associated actor, along a spline.
Default settings will provide a follow from start to end of the Spline. However, the start and end offsets could
make the actor trace intermediate paths along the spline.

**C++ Source:**

- **Plugin**: MoverExamples

- **Module**: MoverExamples

- **File**: FollowSplineMode.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `behaviour_type` (InterpToBehaviourType): [Read-Write] Follow Mode for Path Following

- `constant_follow_velocity` (bool): [Read-Write] Should Mover follow spline with constant velocity

- `control_spline` (SplineComponent): [Read-Only]

- `custom_duration_seconds_override` (float): [Read-Write] If greater than zero, the follow motion would map the spline time to this duration.

- `end_offset` (SplineOffsetRangeInput): [Read-Write] Optional end offset to define ranged follow

- `gameplay_tags` (GameplayTagContainer): [Read-Write] A list of gameplay tags associated with this movement mode

- `interpolation_curve` (CurveFloat): [Read-Write] Optional Interpolation curve to dictate the speed and position for follow

- `orient_mover_to_movement` (bool): [Read-Write] Should Mover face in the direction of movement at all times

- `rotation_type` (FollowSplineRotationType): [Read-Write] Rotation Mode for Path Following

- `shared_settings_classes` (Array[type(Class)]): [Read-Write] Settings object type that this mode depends on. May be shared with other movement modes. When the mode is added to a Mover Component, it will create a shared instance of this settings class.

- `start_offset` (SplineOffsetRangeInput): [Read-Write] Optional starting offset to define ranged follow

- `start_reveresed` (bool): [Read-Write] Should the mover start following from the End

- `supports_async` (bool): [Read-Write] Whether this movement mode supports being part of an asynchronous movement simulation (running concurrently with the gameplay thread)
Specifically for the GenerateMove and SimulationTick functions

- `transitions` (Array[BaseMovementModeTransition]): [Read-Write] Transition checks for the current mode. Evaluated in order, stopping at the first successful transition check



---

_property_ `behaviour_type`: InterpToBehaviourType

[Read-Write] Follow Mode for Path Following

**Type:**

( InterpToBehaviourType)


---

_property_ `constant_follow_velocity`: bool

[Read-Write] Should Mover follow spline with constant velocity

**Type:**

( bool)


---

_property_ `control_spline`: SplineComponent

[Read-Only]

**Type:**

( SplineComponent)


---

_property_ `custom_duration_seconds_override`: float

[Read-Write] If greater than zero, the follow motion would map the spline time to this duration.

**Type:**

( float)


---

_property_ `end_offset`: SplineOffsetRangeInput

[Read-Write] Optional end offset to define ranged follow

**Type:**

( SplineOffsetRangeInput)


---

_property_ `interpolation_curve`: CurveFloat

[Read-Write] Optional Interpolation curve to dictate the speed and position for follow

**Type:**

( CurveFloat)


---

_property_ `orient_mover_to_movement`: bool

[Read-Write] Should Mover face in the direction of movement at all times

**Type:**

( bool)


---

_property_ `rotation_type`: FollowSplineRotationType

[Read-Write] Rotation Mode for Path Following

**Type:**

( FollowSplineRotationType)


---

**set_control_spline**( _spline_provider_actor_, _offset=[0.000000, SplineOffsetUnit.PERCENTAGE]_) → `None`

Set Control Spline

Parameters:

- **spline\_provider\_actor** ( _Actor_)

- **offset** ( _SplineOffsetRangeInput_)



---

_property_ `start_offset`: SplineOffsetRangeInput

[Read-Write] Optional starting offset to define ranged follow

**Type:**

( SplineOffsetRangeInput)


---

_property_ `start_reveresed`: bool

[Read-Write] Should the mover start following from the End

**Type:**

( bool)

### Table of Contents

- `unreal.FollowSplineMode`
  - `FollowSplineMode`
    - `FollowSplineMode.behaviour_type`
    - `FollowSplineMode.constant_follow_velocity`
    - `FollowSplineMode.control_spline`
    - `FollowSplineMode.custom_duration_seconds_override`
    - `FollowSplineMode.end_offset`
    - `FollowSplineMode.interpolation_curve`
    - `FollowSplineMode.orient_mover_to_movement`
    - `FollowSplineMode.rotation_type`
    - `FollowSplineMode.set_control_spline()`
    - `FollowSplineMode.start_offset`
    - `FollowSplineMode.start_reveresed`