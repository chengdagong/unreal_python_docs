# unreal.MetaHumanIdentityCameraFrame

```python
class unreal.MetaHumanIdentityCameraFrame(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``MetaHumanIdentityPromotedFrame``


MetaHuman Identity Camera Frame

**C++ Source:**

- **Plugin**: MetaHuman

- **Module**: MetaHumanIdentity

- **File**: MetaHumanIdentityPromotedFrames.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `camera_view_fov` (float): [Read-Write] The Camera FoV from when the view was promoted

- `contour_data` (MetaHumanContourData): [Read-Write] Contour data class that holds all the data for curves and control vertices

- `contour_tracker` (MetaHumanFaceContourTrackerAsset): [Read-Write] The tracker that can be used to track landmarks on the data represented by this Promoted Frame

- `depth_map_diagnostics` (DepthMapDiagnosticsResult): [Read-Only] The depth-map diagnostics result for the frame

- `fixed_ev100` (float): [Read-Write] The EV100 value to used for this promoted frame

- `frame_name` (Text): [Read-Write] The name of frame as given by the user

- `head_alignment` (Transform): [Read-Only] The alignment of the conformal mesh associated with this promoted frame

- `is_front_view` (bool): [Read-Write] Whether this promoted frame is front view

- `is_head_alignment_set` (bool): [Read-Only] Do we have a valid alignment of the conformal mesh associated with this promoted frame

- `is_navigation_locked` (bool): [Read-Write] Whether or not the navigation is locked for this Promoted frame

- `look_at_location` (Vector): [Read-Write] The current camera LookAt position for this Promoted Frame

- `use_to_solve` (bool): [Read-Write] Whether or not the markers (landmarks) of this Promoted Frame are active

- `view_location` (Vector): [Read-Write] The current camera location for this Promoted Frame

- `view_mode` (ViewModeIndex): [Read-Write] The View Mode from when the frame was promoted

- `view_rotation` (Rotator): [Read-Write] The current camera rotation for this Promoted Frame


### Table of Contents

- `unreal.MetaHumanIdentityCameraFrame`
  - `MetaHumanIdentityCameraFrame`