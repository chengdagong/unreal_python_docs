# unreal.MoviePipelineObjectIdPassIdType

```python
class unreal.MoviePipelineObjectIdPassIdType
```


**Bases:** ``EnumBase``


EMovie Pipeline Object Id Pass Id Type

**C++ Source:**

- **Plugin**: MoviePipelineMaskRenderPass

- **Module**: MoviePipelineMaskRenderPass

- **File**: MoviePipelineObjectIdUtils.h


ACTOR _: MoviePipelineObjectIdPassIdType_ _=Ellipsis_

Grouped by Actor Name, all materials for a given actor are merged together, and all actors with that name are merged together as well.

**Type:**

2

ACTOR\_WITH\_HIERARCHY _: MoviePipelineObjectIdPassIdType_ _=Ellipsis_

Grouped by Actor Name and Folder Hierarchy. This means actors with the same name in different folders will not be merged together.

**Type:**

3

FOLDER _: MoviePipelineObjectIdPassIdType_ _=Ellipsis_

Grouped by Folder Name. All actors within a given folder hierarchy in the World Outliner are merged together.

**Type:**

4

FULL _: MoviePipelineObjectIdPassIdType_ _=Ellipsis_

As much information as the renderer can provide - unique per material per primitive in the world.

**Type:**

0

LAYER _: MoviePipelineObjectIdPassIdType_ _=Ellipsis_

Grouped by Actor Layer (the first layer found in the AActor::Layers array). May not do what you expect if an actor belongs to multiple layers.
If used within a graph, this does NOT refer to the layer within the graph.

In scripting, this option is referred to as “Layer” and not “ActorLayer”.

**Type:**

5

MATERIAL _: MoviePipelineObjectIdPassIdType_ _=Ellipsis_

Grouped by material name. This means different objects that use the same material will be merged.

**Type:**

1

### Table of Contents

- `unreal.MoviePipelineObjectIdPassIdType`
  - `MoviePipelineObjectIdPassIdType`
    - `MoviePipelineObjectIdPassIdType.ACTOR`
    - `MoviePipelineObjectIdPassIdType.ACTOR_WITH_HIERARCHY`
    - `MoviePipelineObjectIdPassIdType.FOLDER`
    - `MoviePipelineObjectIdPassIdType.FULL`
    - `MoviePipelineObjectIdPassIdType.LAYER`
    - `MoviePipelineObjectIdPassIdType.MATERIAL`