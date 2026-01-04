# unreal.SplineMovementPathPattern

```python
class unreal.SplineMovementPathPattern(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``PathedMovementPatternBase``


Spline Movement Path Pattern

**C++ Source:**

- **Plugin**: Mover

- **Module**: Mover

- **File**: SplineMovementPathPattern.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `apply_spline_scaling` (bool): [Read-Write]

- `custom_easing_curve` (CurveFloat): [Read-Write] If using a custom ease, this is the curve that will be used. If blank, will fall back to standard linear interpolation.

- `debug_draw_pattern` (bool): [Read-Write] True to draw debug lines for this specific pattern in editor views

- `easing` (AlphaBlendOption): [Read-Write] The kind of easing to apply when traveling along the path

- `end_at_path_progress` (float): [Read-Write] The overall path progress when this pattern should complete, where 0 is the start of the path and 1 is the end. Must be greater than StartAtProgress.

- `lower_bound` (float): [Read-Write] How far into the spline the movement path actually begins.

- `num_loops_per_path` (int32): [Read-Write] The number of loops to complete within the active span of this pattern (i.e. between StartAtProgress and EndAtProgress)
on a single run along the full aggregate path. Setting to 0 effectively disables this pattern.

- `offsets_modify_duration` (bool): [Read-Write] If true, the path duration will be shortened according to how much of the spline is not being followed.
If false (default), the path duration is unchanged, so the object will move slower when the usable spline range is reduced.

- `orient_component_to_path` (bool): [Read-Write] If true, the component will be rotated to face in the direction of this pattern’s motion.
To have the component face in the direction of the aggregate path, enable this on all movement patterns.

- `pattern_debug_draw_color` (Color): [Read-Write] The color used for debug draws of this pattern

- `per_loop_behavior` (PathedPhysicsPlaybackBehavior): [Read-Write] Playback behavior per loop of this pattern

- `rotation_masks` (uint8): [Read-Write] Along which axes is this pattern disallowed from modifying the rotation of the updated component?

- `scale_masks` (uint8): [Read-Write] Along which axes is this pattern disallowed from modifying the scale of the updated component?

- `spline_component_ref` (ComponentReference): [Read-Write] Optional property to specify the spline component that defines the path to follow. If blank, we’ll use the first spline component we find in this actor.
This is only necessary to set if you have multiple spline components on the actor, or want to follow a spline on an external actor.

- `start_after_previous_pattern` (bool): [Read-Write] If true, this pattern will not begin to take effect until the previous pattern has completed.
Note: If true and the previous pattern’s EndAtPathProgress is 1, this pattern will never start.

- `start_at_path_progress` (float): [Read-Write] The overall path progress when this pattern should begin, where 0 is the start of the path and 1 is the end. Must be less than EndAtProgress.

- `translation_masks` (uint8): [Read-Write] Along which axes is this pattern disallowed from modifying the translation/location of the updated component?

- `upper_bound` (float): [Read-Write] How far into the spline the movement path ends. Must be greater than the lower bound.


### Table of Contents

- `unreal.SplineMovementPathPattern`
  - `SplineMovementPathPattern`