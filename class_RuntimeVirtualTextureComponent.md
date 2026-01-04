# unreal.RuntimeVirtualTextureComponent

```python
class unreal.RuntimeVirtualTextureComponent(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``SceneComponent``


Component used to place a URuntimeVirtualTexture in the world.

**C++ Source:**

- **Module**: Engine

- **File**: RuntimeVirtualTextureComponent.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `absolute_location` (bool): [Read-Write] If RelativeLocation should be considered relative to the world, rather than the parent

- `absolute_rotation` (bool): [Read-Write] If RelativeRotation should be considered relative to the world, rather than the parent

- `absolute_scale` (bool): [Read-Write] If RelativeScale3D should be considered relative to the world, rather than the parent

- `asset_user_data` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `asset_user_data_editor_only` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `auto_activate` (bool): [Read-Write] Whether the component is activated at creation or must be explicitly activated.

- `bounds_align_actor` (Actor): [Read-Write] Actor to align rotation to. If set this actor is always included in the bounds calculation.

- `build_streaming_mips_button` (bool): [Read-Only] Placeholder for details customization button.

- `can_ever_affect_navigation` (bool): [Read-Write] Whether this component can potentially influence navigation

- `component_tags` (Array[Name]): [Read-Write] Array of tags that can be used for grouping and categorizing. Can also be accessed from scripting.

- `detail_mode` (DetailMode): [Read-Write] Set the required detail level of this component.
It will be deleted or made invisible if the world’s detail level is higher, based on platform and scalability settings.
For example, a detail mode of High may prevent this component from loading on mobile platforms.

- `editable_when_inherited` (bool): [Read-Write] True if this component can be modified when it was inherited from a parent actor class

- `enable_for_nanite_only` (bool): [Read-Write] Enable the virtual texture only when Nanite is enabled. Can be used for a Displacement virtual texture with Nanite tessellation.

- `enable_in_game_per_platform` (PerPlatformBool): [Read-Write] Per platform overrides for enabling the virtual texture. Only affects In-Game and PIE.

- `enable_scalability` (bool): [Read-Write] Set to true to enable scalability settings for the virtual texture.

- `expand_bounds` (float): [Read-Write] Amount to expand the Bounds during calculation.

- `hidden_in_game` (bool): [Read-Write] Whether to hide the primitive in game, if the primitive is Visible.

- `hide_primitives` (bool): [Read-Write] Hide primitives in the main pass. Hidden primitives will be those that draw to this virtual texture with ‘Draw in Main Pass’ set to ‘From Virtual Texture’.

- `is_editor_only` (bool): [Read-Write] If true, the component will be excluded from non-editor builds

- `lossy_compression_amount` (TextureLossyCompressionAmount): [Read-Write] How aggressively should any relevant lossy compression be applied.
For compressors that support EncodeSpeed (i.e. Oodle), this is only applied if enabled (see Project Settings -> Texture Encoding).
Note that this is in addition to any unavoidable loss due to the target format. Selecting “No Lossy Compression” will not result in zero distortion for BCn formats.

- `min_in_game_material_quality` (RuntimeVirtualTextureMaterialQuality): [Read-Write] The minimum material quality for which we enable the virtual texture. Only affects In-Game and PIE.

- `mobility` (ComponentMobility): [Read-Write] How often this component is allowed to move, used to make various optimizations. Only safe to set in constructor.

- `on_component_activated` (ActorComponentActivatedSignature): [Read-Write] Called when the component has been activated, with parameter indicating if it was from a reset

- `on_component_deactivated` (ActorComponentDeactivateSignature): [Read-Write] Called when the component has been deactivated

- `physics_volume_changed_delegate` (PhysicsVolumeChanged): [Read-Write] Delegate that will be called when PhysicsVolume has been changed \*

- `primary_component_tick` (ActorComponentTickFunction): [Read-Write] Main tick function for the Component

- `relative_location` (Vector): [Read-Write] Location of the component relative to its parent

- `relative_rotation` (Rotator): [Read-Write] Rotation of the component relative to its parent

- `relative_scale3d` (Vector): [Read-Write] Non-uniform scaling of the component relative to its parent.
Note that scaling is always applied in local space (no shearing etc)

- `replicate_using_registered_sub_object_list` (bool): [Read-Write] When true the replication system will only replicate the registered subobjects list
When false the replication system will instead call the virtual ReplicateSubObjects() function where the subobjects need to be manually replicated.

- `replicates` (bool): [Read-Write] Is this component currently replicating? Should the network code consider it for replication? Owning Actor must be replicating first!

- `scalability_group` (uint32): [Read-Write] Group index of the scalability settings to use for the virtual texture.

- `set_bounds_button` (bool): [Read-Only] Placeholder for details customization button.

- `should_update_physics_volume` (bool): [Read-Write] Whether or not the cached PhysicsVolume this component overlaps should be updated when the component is moved.
see: GetPhysicsVolume()

- `snap_bounds_to_landscape` (bool): [Read-Write] If the Bounds Align Actor is a Landscape then this will snap the bounds so that virtual texture texels align with landscape vertex positions.

- `stream_low_mips` (int32): [Read-Write] Number of streaming low mips to build for the virtual texture.

- `streaming_mips_fixed_color` (LinearColor): [Read-Write] Fixed color to use when building the streaming low mips. This only affects BaseColor and Displacement attributes. The Red channel is used for fixed Displacement.

- `streaming_texture` (VirtualTextureBuilder): [Read-Write] Texture object containing streamed low mips. This can reduce rendering update cost.

- `use_attach_parent_bound` (bool): [Read-Write] If true, this component uses its parents bounds when attached.
This can be a significant optimization with many components attached together.

- `use_min_material_quality` (bool): [Read-Write] Use a minimum material quality to determine if we enable the virtual texture.

- `use_streaming_mips_fixed_color` (bool): [Read-Write] Build the streaming low mips using a fixed color.

- `use_streaming_mips_in_editor_mode` (RuntimeVirtualTextureUseStreamingMipsInEditorMode): [Read-Write] Use streaming low mips when rendering this runtime virtual texture in the editor. Allows to visualize the baked streaming low mips.
r.VT.RVT.StreamingMips.UseInEditor can also be used to allow this across all RVT components (for debugging purposes)

- `use_streaming_mips_only` (bool): [Read-Write] Whenever streaming low mips are in use, only show the streaming mips and never show runtime generated pages.

- `virtual_texture` (RuntimeVirtualTexture): [Read-Write] The virtual texture object to use.

- `visible` (bool): [Read-Write] Whether to completely draw the primitive; if false, the primitive is not drawn, does not cast a shadow.



---

**invalidate**( _world_bounds_, _invalidate_priority=VTInvalidatePriority.HIGH_) → `None`

This function marks an area of the runtime virtual texture as dirty.

Parameters:

- **world\_bounds** ( _BoxSphereBounds_) – : The world space bounds of the pages to invalidate.

- **invalidate\_priority** ( _VTInvalidatePriority_) – Allows the pages affected by this area to get processed in priority. This allows increased responsiveness when there are more pages being updated than can be handled in a given frame (throttling)



---

_property_ `lossy_compression_amount`: TextureLossyCompressionAmount

[Read-Write] How aggressively should any relevant lossy compression be applied.
For compressors that support EncodeSpeed (i.e. Oodle), this is only applied if enabled (see Project Settings -> Texture Encoding).
Note that this is in addition to any unavoidable loss due to the target format. Selecting “No Lossy Compression” will not result in zero distortion for BCn formats.

**Type:**

( TextureLossyCompressionAmount)


---

**request_preload**( _world_bounds_, _level_) → `None`

Request preload of an area of the runtime virtual texture at a given mip level.

Parameters:

- **world\_bounds** ( _BoxSphereBounds_) – : The world space bounds of the pages to preload.

- **level** ( _int32_) – : The mip map level to preload.



---

_property_ `streaming_mips_fixed_color`: LinearColor

[Read-Only] Fixed color to use when building the streaming low mips. This only affects BaseColor and Displacement attributes. The Red channel is used for fixed Displacement.

**Type:**

( LinearColor)


---

_property_ `streaming_texture`: VirtualTextureBuilder

[Read-Only] Texture object containing streamed low mips. This can reduce rendering update cost.

**Type:**

( VirtualTextureBuilder)


---

_property_ `use_streaming_mips_fixed_color`: bool

[Read-Only] Build the streaming low mips using a fixed color.

**Type:**

( bool)


---

_property_ `virtual_texture`: RuntimeVirtualTexture

[Read-Only] The virtual texture object to use.

**Type:**

( RuntimeVirtualTexture)

### Table of Contents

- `unreal.RuntimeVirtualTextureComponent`
  - `RuntimeVirtualTextureComponent`
    - `RuntimeVirtualTextureComponent.invalidate()`
    - `RuntimeVirtualTextureComponent.lossy_compression_amount`
    - `RuntimeVirtualTextureComponent.request_preload()`
    - `RuntimeVirtualTextureComponent.streaming_mips_fixed_color`
    - `RuntimeVirtualTextureComponent.streaming_texture`
    - `RuntimeVirtualTextureComponent.use_streaming_mips_fixed_color`
    - `RuntimeVirtualTextureComponent.virtual_texture`