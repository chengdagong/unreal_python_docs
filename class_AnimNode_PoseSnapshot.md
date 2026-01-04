# unreal.AnimNode_PoseSnapshot

```python
class unreal.AnimNode_PoseSnapshot(snapshot_name:Name='None', snapshot:PoseSnapshot=Ellipsis, mode:SnapshotSourceMode=Ellipsis)
```


**Bases:** ``AnimNode_Base``


Provide a snapshot pose, either from the internal named pose cache or via a supplied snapshot

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_PoseSnapshot.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `mode` (SnapshotSourceMode): [Read-Write] How to access the snapshot

- `snapshot` (PoseSnapshot): [Read-Write] Snapshot to use. This should be populated at first by calling SnapshotPose

- `snapshot_name` (Name): [Read-Write] The name of the snapshot previously stored with SavePoseSnapshot



---

_property_ `mode`: SnapshotSourceMode

[Read-Write] How to access the snapshot

**Type:**

( SnapshotSourceMode)


---

_property_ `snapshot`: PoseSnapshot

[Read-Write] Snapshot to use. This should be populated at first by calling SnapshotPose

**Type:**

( PoseSnapshot)


---

_property_ `snapshot_name`: Name

[Read-Write] The name of the snapshot previously stored with SavePoseSnapshot

**Type:**

( Name)

### Table of Contents

- `unreal.AnimNode_PoseSnapshot`
  - `AnimNode_PoseSnapshot`
    - `AnimNode_PoseSnapshot.mode`
    - `AnimNode_PoseSnapshot.snapshot`
    - `AnimNode_PoseSnapshot.snapshot_name`