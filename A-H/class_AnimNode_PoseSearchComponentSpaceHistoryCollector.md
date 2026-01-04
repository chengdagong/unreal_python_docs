# unreal.AnimNode_PoseSearchComponentSpaceHistoryCollector

```python
class unreal.AnimNode_PoseSearchComponentSpaceHistoryCollector(pose_count:int=0, sampling_interval:float=0.0, root_bone_recovery_time:float=0.0, root_bone_translation_recovery_ratio:float=0.0, root_bone_rotation_recovery_ratio:float=0.0, trajectory_history_count:int=0, trajectory_prediction_count:int=0, prediction_sampling_interval:float=0.0, source:ComponentSpacePoseLink=\[\])
```


**Bases:** ``AnimNode_PoseSearchHistoryCollector_Base``


Anim Node Pose Search Component Space History Collector

**C++ Source:**

- **Plugin**: PoseSearch

- **Module**: PoseSearch

- **File**: AnimNode\_PoseSearchHistoryCollector.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `collected_bones` (Array[BoneReference]): [Read-Write]

- `collected_curves` (Array[Name]): [Read-Write]

- `debug_color` (LinearColor): [Read-Write]

- `generate_trajectory` (bool): [Read-Write] if true Trajectory the pose history node will generate the trajectory using the TrajectoryData parameters instead of relying on the input Trajectory
Experimental, this feature might be removed without warning, not for production use

- `pose_count` (int32): [Read-Write] The maximum amount of poses that can be stored

- `prediction_sampling_interval` (float): [Read-Write] if bGenerateTrajectory is true, this is the sampling interval between trajectory future (prediction) samples

- `reset_on_becoming_relevant` (bool): [Read-Write] Reset the pose history if it has become relevant to the graph after not being updated on previous frames.

- `root_bone_recovery_time` (float): [Read-Write] time in seconds to recover to the reference skeleton root bone transform by RootBoneTranslationRecoveryRatio and RootBoneRotationRecoveryRatio
from any eventual root bone modification. if zero the behaviour will be disabled
Experimental, this feature might be removed without warning, not for production use

- `root_bone_rotation_recovery_ratio` (float): [Read-Write] ratio to recover to the reference skeleton root bone rotation from any eventual root bone modification. zero for no recovery, 1 for full recovery

- `root_bone_translation_recovery_ratio` (float): [Read-Write] ratio to recover to the reference skeleton root bone translation from any eventual root bone modification. zero for no recovery, 1 for full recovery

- `sampling_interval` (float): [Read-Write] how often in seconds poses are collected (if 0, it will collect every update)

- `source` (ComponentSpacePoseLink): [Read-Write]

- `store_scales` (bool): [Read-Write] if true pose scales will be cached, otherwise implied to be unitary scales

- `trajectory_data` (PoseSearchTrajectoryData): [Read-Write] if bGenerateTrajectory is true, TrajectoryData contains the tuning parameters to generate the trajectory

- `trajectory_history_count` (int32): [Read-Write] if bGenerateTrajectory is true, this is the number of trajectory past (collected) samples

- `trajectory_prediction_count` (int32): [Read-Write] if bGenerateTrajectory is true, this is the number of trajectory future (prediction) samples

- `trajectory_speed_multiplier` (float): [Read-Write] Input Trajectory velocity will be multiplied by TrajectorySpeedMultiplier: values below 1 will result in selecting animation slower than requested from the original Trajectory

- `transform_trajectory` (TransformTrajectory): [Read-Write] Input Trajectory samples for pose search queries in Motion Matching. These are expected to be in the world space of the SkeletalMeshComponent.
the trajectory sample with AccumulatedSeconds equals to zero (Trajectory.Samples[i].AccumulatedSeconds) is the sample of the previous frame of simulation (since MM works by matching the previous character pose)



---

_property_ `source`: ComponentSpacePoseLink

[Read-Write]

**Type:**

( ComponentSpacePoseLink)

### Table of Contents

- `unreal.AnimNode_PoseSearchComponentSpaceHistoryCollector`
  - `AnimNode_PoseSearchComponentSpaceHistoryCollector`
    - `AnimNode_PoseSearchComponentSpaceHistoryCollector.source`