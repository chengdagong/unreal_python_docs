# unreal.NiagaraDataInterfaceSkeletalMesh

```python
class unreal.NiagaraDataInterfaceSkeletalMesh(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``NiagaraDataInterface``


Data Interface allowing sampling of skeletal meshes.

**C++ Source:**

- **Plugin**: Niagara

- **Module**: Niagara

- **File**: NiagaraDataInterfaceSkeletalMesh.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `component_tags` (Array[Name]): [Read-Write] If defined, the supplied tags will be used to identify a valid component

- `default_mesh` (SkeletalMesh): [Read-Write] Mesh used to sample from when not overridden by a source actor from the scene. This mesh is NOT removed from cooked builds.

- `exclude_bone` (bool): [Read-Write]

- `exclude_bone_name` (Name): [Read-Write] Optionally remove a single bone from Random / Random Unfiltered access.
You can still include this bone in filtered list and access using the direct index functionality.

- `filtered_bones` (Array[Name]): [Read-Write] Set of filtered bones that can be used for sampling. Select from these with GetFilteredBoneAt and RandomFilteredBone.

- `filtered_sockets` (Array[Name]): [Read-Write] Set of filtered sockets that can be used for sampling. Select from these with GetFilteredSocketAt and RandomFilteredSocket.

- `mesh_user_parameter` (NiagaraUserParameterBinding): [Read-Write] Reference to a user parameter if we’re reading one.

- `preview_mesh` (SkeletalMesh): [Read-Write] Mesh used to sample from when not overridden by a source actor from the scene. Only available in editor for previewing. This is removed in cooked builds.

- `read_deformed_geometry` (bool): [Read-Write] Overrides the project setting and allows you to opt out of reading from deformed geometry.
These is not performance gain from doing this, the branches will still exist in the generated code.

- `require_current_frame_data` (bool): [Read-Write] When this option is disabled, we use the previous frame’s data for the skeletal mesh and can often issue the simulation early. This greatly

reduces overhead and allows the game thread to run faster, but comes at a tradeoff if the dependencies might leave gaps or other visual artifacts.

- `sampling_regions` (Array[Name]): [Read-Write] Sampling regions on the mesh from which to sample. Leave this empty to sample from the whole mesh.

- `skinning_mode` (NDISkeletalMesh\_SkinningMode): [Read-Write] Selects which skinning mode to use, for most cases Skin On The Fly will cover your requirements, see individual tooltips for more information.

- `soft_source_actor` (Actor): [Read-Write] The source actor from which to sample. Takes precedence over the direct mesh. Note that this can only be set when used as a user variable on a component in the world.

- `source_mode` (NDISkeletalMesh\_SourceMode): [Read-Write] Controls how to retrieve the Skeletal Mesh Component to attach to.

- `uv_set_index` (int32): [Read-Write]

- `whole_mesh_lod` (int32): [Read-Write] If no regions are specified, we’ll sample the whole mesh at this LODIndex.
  -1 will use the lowest quality LOD available, i.e. Number of LODs - 1.


### Table of Contents

- `unreal.NiagaraDataInterfaceSkeletalMesh`
  - `NiagaraDataInterfaceSkeletalMesh`