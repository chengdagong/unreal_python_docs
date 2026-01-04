# unreal.BoneAnimationTrack

```python
class unreal.BoneAnimationTrack(internal_track_data:RawAnimSequenceTrack=\[\], bone_tree_index:int=0, name:Name='None')
```


**Bases:** ``StructBase``


Structure encapsulating a single bone animation track.

**C++ Source:**

- **Module**: Engine

- **File**: IAnimationDataModel.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `bone_tree_index` (int32): [Read-Only] Index corresponding to the bone this track corresponds to within the target USkeleton

- `internal_track_data` (RawAnimSequenceTrack): [Read-Only] Internally stored data representing the animation bone data

- `name` (Name): [Read-Only] Name of the bone this track corresponds to



---

_property_ `bone_tree_index`: int

[Read-Only] Index corresponding to the bone this track corresponds to within the target USkeleton

**Type:**

(int32)


---

_property_ `internal_track_data`: RawAnimSequenceTrack

[Read-Only] Internally stored data representing the animation bone data

**Type:**

( RawAnimSequenceTrack)


---

_property_ `name`: Name

[Read-Only] Name of the bone this track corresponds to

**Type:**

( Name)

### Table of Contents

- `unreal.BoneAnimationTrack`
  - `BoneAnimationTrack`
    - `BoneAnimationTrack.bone_tree_index`
    - `BoneAnimationTrack.internal_track_data`
    - `BoneAnimationTrack.name`