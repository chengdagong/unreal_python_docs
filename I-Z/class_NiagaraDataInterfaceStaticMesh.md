# unreal.NiagaraDataInterfaceStaticMesh

```python
class unreal.NiagaraDataInterfaceStaticMesh(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``NiagaraDataInterface``


Data Interface allowing sampling of static meshes.

**C++ Source:**

- **Plugin**: Niagara

- **Module**: Niagara

- **File**: NiagaraDataInterfaceStaticMesh.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `allow_sampling_from_streaming_lo_ds` (bool): [Read-Write] When true, we allow this DI to sample from streaming LODs. Selectively overriding the CVar fx.Niagara.NDIStaticMesh.UseInlineLODsOnly.

- `capture_transforms_per_frame` (bool): [Read-Write] If true we capture the transforms from the mesh component each frame.

- `default_mesh` (StaticMesh): [Read-Write] Mesh used to sample from when not overridden by a source actor from the scene. This mesh is NOT removed from cooked builds.

- `filtered_sockets` (Array[Name]): [Read-Write] List of filtered sockets to use.

- `instance_index` (int32): [Read-Write] When attached to an Instanced Static Mesh, which instance should be read from.

- `lod_index` (int32): [Read-Write] Static Mesh LOD to sample.
When the desired LOD is not available, the next available LOD is used.
When LOD Index is negative, Desired LOD = Num LODs - LOD Index.

- `lod_index_user_parameter` (NiagaraUserParameterBinding): [Read-Write] Reference to a user parameter if we’re reading one.

- `mesh_parameter_binding` (NiagaraUserParameterBinding): [Read-Write] Mesh parameter binding can be either an Actor (in which case we find the component), static mesh component or a static mesh.

- `preview_mesh` (StaticMesh): [Read-Write] Mesh used to sample from when not overridden by a source actor from the scene. Only available in editor for previewing. This is removed in cooked builds.

- `section_filter` (NDIStaticMeshSectionFilter): [Read-Write] Array of filters the can be used to limit sampling to certain sections of the mesh.

- `soft_source_actor` (Actor): [Read-Write] The source actor from which to sample. Takes precedence over the direct mesh. Note that this can only be set when used as a user variable on a component in the world.

- `source_mode` (NDIStaticMesh\_SourceMode): [Read-Write] Controls how to retrieve the Static Mesh Component to attach to.

- `use_physics_body_velocity` (bool): [Read-Write] If true then the mesh velocity is taken from the mesh component’s physics data. Otherwise it will be calculated by diffing the component transforms between ticks, which is more reliable but won’t work on the first frame.



---

_classmethod_ set_niagara_static_mesh_di_instance_index( _niagara_system_, _user_parameter_name_, _new_instance_index_)→None

Set Niagara Static Mesh DIInstance Index

Parameters:

- **niagara\_system** ( _NiagaraComponent_)

- **user\_parameter\_name** ( _Name_)

- **new\_instance\_index** ( _int32_)


### Table of Contents

- `unreal.NiagaraDataInterfaceStaticMesh`
  - `NiagaraDataInterfaceStaticMesh`
    - `NiagaraDataInterfaceStaticMesh.set_niagara_static_mesh_di_instance_index()`