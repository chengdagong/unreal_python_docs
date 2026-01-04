# unreal.AnimNode_RigMapper

```python
class unreal.AnimNode_RigMapper(source_pose:PoseLink=\[\], definitions:None=\[\], lod_threshold:int=0, alpha:float=0.0)
```


**Bases:** ``AnimNode_Base``


Anim Node Rig Mapper

**C++ Source:**

- **Plugin**: RigMapper

- **Module**: RigMapper

- **File**: AnimNode\_RigMapper.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alpha` (float): [Read-Write]

- `definitions` (Array[RigMapperDefinition]): [Read-Write]

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

- `source_pose` (PoseLink): [Read-Write]



---

_property_ `alpha`: float

[Read-Write]

**Type:**

( float)


---

_property_ `definitions`: None

[Read-Write]

**Type:**

( Array\ [RigMapperDefinition])


---

_property_ `lod_threshold`: int

[Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

**Type:**

(int32)


---

_property_ `source_pose`: PoseLink

[Read-Write]

**Type:**

( PoseLink)

### Table of Contents

- `unreal.AnimNode_RigMapper`
  - `AnimNode_RigMapper`
    - `AnimNode_RigMapper.alpha`
    - `AnimNode_RigMapper.definitions`
    - `AnimNode_RigMapper.lod_threshold`
    - `AnimNode_RigMapper.source_pose`