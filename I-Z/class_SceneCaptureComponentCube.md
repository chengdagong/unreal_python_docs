# unreal.SceneCaptureComponentCube

```python
class unreal.SceneCaptureComponentCube(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``SceneCaptureComponent``


Used to capture a ‘snapshot’ of the scene from a 6 planes and feed it to a render target.

**C++ Source:**

- **Module**: Engine

- **File**: SceneCaptureComponentCube.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `absolute_location` (bool): [Read-Write] If RelativeLocation should be considered relative to the world, rather than the parent

- `absolute_rotation` (bool): [Read-Write] If RelativeRotation should be considered relative to the world, rather than the parent

- `absolute_scale` (bool): [Read-Write] If RelativeScale3D should be considered relative to the world, rather than the parent

- `always_persist_rendering_state` (bool): [Read-Write] Whether to persist the rendering state even if bCaptureEveryFrame==false. This allows velocities for Motion Blur and Temporal AA to be computed.

- `asset_user_data` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `asset_user_data_editor_only` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `auto_activate` (bool): [Read-Write] Whether the component is activated at creation or must be explicitly activated.

- `can_ever_affect_navigation` (bool): [Read-Write] Whether this component can potentially influence navigation

- `capture_every_frame` (bool): [Read-Write] Whether to update the capture’s contents every frame. If disabled, the component will render once on load and then only when moved.

- `capture_gpu_next_render` (bool): [Read-Write] Capture a GPU frame for this scene capture, next time it renders (capture program must be connected).

- `capture_on_movement` (bool): [Read-Write] Whether to update the capture’s contents on movement. Disable if you are going to capture manually from blueprint.

- `capture_rotation` (bool): [Read-Write] Preserve the rotation of the actor when updating the capture. The default behavior is to capture the cube aligned to the world axis system.

- `capture_sort_priority` (int32): [Read-Write] Capture priority within the frame to sort scene capture on GPU to resolve interdependencies between multiple capture components. Highest come first.

- `capture_source` (SceneCaptureSource): [Read-Write]

- `collection_transform` (MaterialParameterCollection): [Read-Write] Store WorldToLocal and/or Projection matrices (2D capture only) to a Material Parameter Collection on render.

- `collection_transform_projection` (Name): [Read-Write] Parameter name of the first element of the transform in the CollectionTransform Material Parameter Collection set above. Requires space for 4 vectors.

- `collection_transform_world_to_local` (Name): [Read-Write] Parameter name of the first element of the transform in the CollectionTransform Material Parameter Collection set above. Requires space for 5 vectors (large world coordinate transform).

- `component_tags` (Array[Name]): [Read-Write] Array of tags that can be used for grouping and categorizing. Can also be accessed from scripting.

- `detail_mode` (DetailMode): [Read-Write] Set the required detail level of this component.
It will be deleted or made invisible if the world’s detail level is higher, based on platform and scalability settings.
For example, a detail mode of High may prevent this component from loading on mobile platforms.

- `dump_gpu_next_render` (bool): [Read-Write] Run DumpGPU for this scene capture, next time it renders.

- `editable_when_inherited` (bool): [Read-Write] True if this component can be modified when it was inherited from a parent actor class

- `exclude_from_scene_texture_extents` (bool): [Read-Write] Whether this capture should be excluded from tracking scene texture extents. This should be set when this capture is not expected to be
frequently used, especially if the capture resolution is very large. Setting this for a single-use capture will avoid influencing other
scene texture extent decisions and avoid a possible ongoing increase in memory usage.

- `hidden_actors` (Array[Actor]): [Read-Write] The actors to hide in the scene capture.

- `hidden_in_game` (bool): [Read-Write] Whether to hide the primitive in game, if the primitive is Visible.

- `is_editor_only` (bool): [Read-Write] If true, the component will be excluded from non-editor builds

- `lod_distance_factor` (float): [Read-Write] Scales the distance used by LOD. Set to values greater than 1 to cause the scene capture to use lower LODs than the main view to speed up the scene capture pass.

- `max_view_distance_override` (float): [Read-Write] if > 0, sets a maximum render distance override. Can be used to cull distant objects from a reflection if the reflecting plane is in an enclosed area like a hallway or room

- `mobility` (ComponentMobility): [Read-Write] How often this component is allowed to move, used to make various optimizations. Only safe to set in constructor.

- `on_component_activated` (ActorComponentActivatedSignature): [Read-Write] Called when the component has been activated, with parameter indicating if it was from a reset

- `on_component_deactivated` (ActorComponentDeactivateSignature): [Read-Write] Called when the component has been deactivated

- `physics_volume_changed_delegate` (PhysicsVolumeChanged): [Read-Write] Delegate that will be called when PhysicsVolume has been changed \*

- `post_process_blend_weight` (float): [Read-Write] Range (0.0, 1.0) where 0 indicates no effect, 1 indicates full effect.

- `post_process_settings` (PostProcessSettings): [Read-Write]

- `primary_component_tick` (ActorComponentTickFunction): [Read-Write] Main tick function for the Component

- `primitive_render_mode` (SceneCapturePrimitiveRenderMode): [Read-Write] Controls what primitives get rendered into the scene capture.

- `profiling_event_name` (str): [Read-Write] Name of the profiling event.

- `relative_location` (Vector): [Read-Write] Location of the component relative to its parent

- `relative_rotation` (Rotator): [Read-Write] Rotation of the component relative to its parent

- `relative_scale3d` (Vector): [Read-Write] Non-uniform scaling of the component relative to its parent.
Note that scaling is always applied in local space (no shearing etc)

- `replicate_using_registered_sub_object_list` (bool): [Read-Write] When true the replication system will only replicate the registered subobjects list
When false the replication system will instead call the virtual ReplicateSubObjects() function where the subobjects need to be manually replicated.

- `replicates` (bool): [Read-Write] Is this component currently replicating? Should the network code consider it for replication? Owning Actor must be replicating first!

- `should_update_physics_volume` (bool): [Read-Write] Whether or not the cached PhysicsVolume this component overlaps should be updated when the component is moved.
see: GetPhysicsVolume()

- `show_flag_settings` (Array[EngineShowFlagsSetting]): [Read-Write]

- `show_only_actors` (Array[Actor]): [Read-Write] The only actors to be rendered by this scene capture, if PrimitiveRenderMode is set to UseShowOnlyList.

- `texture_target` (TextureRenderTargetCube): [Read-Write] Temporary render target that can be used by the editor.

- `use_attach_parent_bound` (bool): [Read-Write] If true, this component uses its parents bounds when attached.
This can be a significant optimization with many components attached together.

- `use_ray_tracing_if_enabled` (bool): [Read-Write] Whether to use ray tracing for this capture. Ray Tracing must be enabled in the project.

- `view_lighting_channels` (ViewLightingChannels): [Read-Write] View / light masking support. Controls which lights should affect this view.

- `visible` (bool): [Read-Write] Whether to completely draw the primitive; if false, the primitive is not drawn, does not cast a shadow.



---

_property_ `capture_rotation`: bool

[Read-Write] Preserve the rotation of the actor when updating the capture. The default behavior is to capture the cube aligned to the world axis system.

**Type:**

( bool)


---

**capture_scene**() → `None`

Render the scene to the texture target immediately.
This should not be used if bCaptureEveryFrame is enabled, or the scene capture will render redundantly.
If r.SceneCapture.CullByDetailMode is set, nothing will happen if DetailMode is higher than r.DetailMode.


---

_property_ `post_process_blend_weight`: float

[Read-Write] Range (0.0, 1.0) where 0 indicates no effect, 1 indicates full effect.

**Type:**

( float)


---

_property_ `post_process_settings`: PostProcessSettings

[Read-Write]

**Type:**

( PostProcessSettings)


---

_property_ `texture_target`: TextureRenderTargetCube

[Read-Write] Temporary render target that can be used by the editor.

**Type:**

( TextureRenderTargetCube)


---

**update_content**() → `None`

deprecated: ‘update\_content’ was renamed to ‘capture\_scene’.

### Table of Contents

- `unreal.SceneCaptureComponentCube`
  - `SceneCaptureComponentCube`
    - `SceneCaptureComponentCube.capture_rotation`
    - `SceneCaptureComponentCube.capture_scene()`
    - `SceneCaptureComponentCube.post_process_blend_weight`
    - `SceneCaptureComponentCube.post_process_settings`
    - `SceneCaptureComponentCube.texture_target`
    - `SceneCaptureComponentCube.update_content()`