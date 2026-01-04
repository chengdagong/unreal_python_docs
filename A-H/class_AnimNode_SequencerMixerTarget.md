# unreal.AnimNode_SequencerMixerTarget

```python
class unreal.AnimNode_SequencerMixerTarget(source_pose:PoseLink=\[\], target_name:Name='None')
```


**Bases:** ``AnimNode_Base``


Anim Node Sequencer Mixer Target

**C++ Source:**

- **Plugin**: MovieSceneAnimMixer

- **Module**: MovieSceneAnimMixer

- **File**: AnimNode\_SequencerMixerTarget.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `source_pose` (PoseLink): [Read-Write] The source input. This is passed through if there is no animation received from the level sequence, otherwise it’s blended in.

- `target_name` (Name): [Read-Write] The target name for the level sequence to match with when applying its animation.



---

_property_ `source_pose`: PoseLink

[Read-Write] The source input. This is passed through if there is no animation received from the level sequence, otherwise it’s blended in.

**Type:**

( PoseLink)


---

_property_ `target_name`: Name

[Read-Write] The target name for the level sequence to match with when applying its animation.

**Type:**

( Name)

### Table of Contents

- `unreal.AnimNode_SequencerMixerTarget`
  - `AnimNode_SequencerMixerTarget`
    - `AnimNode_SequencerMixerTarget.source_pose`
    - `AnimNode_SequencerMixerTarget.target_name`