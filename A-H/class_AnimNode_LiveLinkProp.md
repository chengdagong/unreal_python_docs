# unreal.AnimNode_LiveLinkProp

```python
class unreal.AnimNode_LiveLinkProp
```


**Bases:** ``AnimNode_Base``


This animnode is exclusively for Mocap props - single bone skeleton meshes. Not exposed to the animation graph.

**C++ Source:**

- **Plugin**: PerformanceCaptureWorkflow

- **Module**: PerformanceCaptureWorkflowRuntime

- **File**: AnimNode\_LiveLinkProp.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `do_live_link_evaluation` (bool): [Read-Write] Bool to control evaluation of animation.

- `dynamic_constraint_offset` (Vector): [Read-Write] Location to apply in parent bone space to offset the incoming Live Link data.

- `input_pose` (PoseLink): [Read-Write] Input pose

- `live_link_subject_name` (LiveLinkSubjectName): [Read-Write] The Live Link subject to use.

- `offset_transform` (Transform): [Read-Write] Transform to apply local space to offset to the incoming Live Link data.


### Table of Contents

- `unreal.AnimNode_LiveLinkProp`
  - `AnimNode_LiveLinkProp`