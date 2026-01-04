# unreal.ChaosPointMovementPathPattern

```python
class unreal.ChaosPointMovementPathPattern(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``ChaosPathedMovementPatternBase``


Movement pattern that moves between explicitly defined points

**C++ Source:**

- **Plugin**: ChaosMover

- **Module**: ChaosMover

- **File**: ChaosPointMovementPathPattern.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `custom_easing_curve` (CurveFloat): [Read-Write] If using a custom ease, this is the curve that will be used. If blank, will fall back to standard linear interpolation.

- `debug_draw_pattern` (bool): [Read-Write] True to draw debug lines for this specific pattern in editor views

- `easing` (AlphaBlendOption): [Read-Write] The kind of easing to apply when traveling along the path

- `end_at_path_progress` (float): [Read-Write] The overall path progress when this pattern should complete, where 0 is the start of the path and 1 is the end. Must be greater than StartAtPathProgress.

- `is_one_way` (bool): [Read-Write] Whether a loop is played one way (0 -> 1) or there and back (0 -> 1 -> 0)

- `loop_offset` (float): [Read-Write] This is an offset within a loop of the pattern, allowing to offset the start of the loop within the path. For example if this is set to 0.2,

a loop will start at 20% of the path (instead of at the start), progress to the end, then wrap around to the start and continue progressing to 20%.
If the path itself is not a loop (if start and end are not the same), then the position will jump abruptly when it wraps around.

- `num_loops_per_path` (int32): [Read-Write] The number of loops to complete within the active span of this pattern (i.e. between StartAtPathProgress and EndAtPathProgress)
on a single run along the full aggregate path. Setting to 0 effectively disables this pattern.

- `orient_component_to_path` (bool): [Read-Write] If true, the component will be rotated to face in the direction of this pattern’s motion.
To have the component face in the direction of the aggregate path, enable this on all movement patterns.

- `path_points` (Array[ChaosPointMovementPathPoint]): [Read-Write] Relative point locations to move toward, in sequence from first to last

- `pattern_debug_draw_color` (Color): [Read-Write] The color used for debug draws of this pattern

- `rotation_masks` (uint8): [Read-Write] Along which axes is this pattern disallowed from modifying the rotation of the updated component?

- `scale_masks` (uint8): [Read-Write] Along which axes is this pattern disallowed from modifying the scale of the updated component?

- `start_after_previous_pattern` (bool): [Read-Write] If true, this pattern will not begin to take effect until the previous pattern has completed.
Note: If true and the previous pattern’s EndAtPathProgress is 1, this pattern will never start.

- `start_at_path_progress` (float): [Read-Write] The overall path progress when this pattern should begin, where 0 is the start of the path and 1 is the end. Must be less than EndAtPathProgress.

- `translation_masks` (uint8): [Read-Write] Along which axes is this pattern disallowed from modifying the translation/location of the updated component?



---

_property_ `path_points`: None

[Read-Write] Relative point locations to move toward, in sequence from first to last

**Type:**

( Array\ [ChaosPointMovementPathPoint])

### Table of Contents

- `unreal.ChaosPointMovementPathPattern`
  - `ChaosPointMovementPathPattern`
    - `ChaosPointMovementPathPattern.path_points`