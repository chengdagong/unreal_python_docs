# unreal.AnimNode_AnimNextGraph

```python
class unreal.AnimNode_AnimNextGraph
```


**Bases:** ``AnimNode_CustomProperty``


Animation node that allows a AnimNextGraph output to be used in an animation graph

**C++ Source:**

- **Plugin**: UAFAnimGraph

- **Module**: UAFAnimGraph

- **File**: AnimNode\_AnimNextGraph.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `animation_graph` (AnimNextAnimationGraph): [Read-Write]

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

- `source_link` (PoseLink): [Read-Write] The input pose we will pass to the graph


### Table of Contents

- `unreal.AnimNode_AnimNextGraph`
  - `AnimNode_AnimNextGraph`