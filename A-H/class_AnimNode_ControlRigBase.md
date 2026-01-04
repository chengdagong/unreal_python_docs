# unreal.AnimNode_ControlRigBase

```python
class unreal.AnimNode_ControlRigBase
```


**Bases:** ``AnimNode_CustomProperty``


Animation node that allows animation ControlRig output to be used in an animation graph

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: AnimNode\_ControlRigBase.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `asset_user_data` (Array[AssetUserData]): [Read-Write]

- `event_queue` (Array[ControlRigAnimNodeEventName]): [Read-Write] The customized event queue to run

- `input_bones_to_transfer` (Array[BoneReference]): [Read-Write] An inclusive list of bones to transfer as part
of the input pose transfer phase.
If this list is empty all bones will be transferred.

- `output_bones_to_transfer` (Array[BoneReference]): [Read-Write] An inclusive list of bones to transfer as part
of the output pose transfer phase.
If this list is empty all bones will be transferred.

- `reset_input_pose_to_initial` (bool): [Read-Write] If this is checked the rig’s pose needs to be reset to its initial
prior to evaluating the rig.

- `source` (PoseLink): [Read-Write]

- `transfer_input_curves` (bool): [Read-Write] If this is checked the curves coming from the AnimBP will be
transferred into the Control Rig.

- `transfer_input_pose` (bool): [Read-Write] If this is checked the bone pose coming from the AnimBP will be
transferred into the Control Rig.

- `transfer_pose_in_global_space` (bool): [Read-Write] Transferring the pose in global space guarantees a global pose match,
while transferring in local space ensures a match of the local transforms.
In general transforms only differ if the hierarchy topology differs
between the Control Rig and the skeleton used in the AnimBP.
Note: Turning this off can potentially improve performance.


### Table of Contents

- `unreal.AnimNode_ControlRigBase`
  - `AnimNode_ControlRigBase`