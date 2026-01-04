# unreal.SceneCaptureComponent2D

```python
class unreal.SceneCaptureComponent2D(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``SceneCaptureComponent``


Used to capture a ‘snapshot’ of the scene from a single plane and feed it to a render target.

**C++ Source:**

- **Module**: Engine

- **File**: SceneCaptureComponent2D.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `absolute_location` (bool): [Read-Write] If RelativeLocation should be considered relative to the world, rather than the parent

- `absolute_rotation` (bool): [Read-Write] If RelativeRotation should be considered relative to the world, rather than the parent

- `absolute_scale` (bool): [Read-Write] If RelativeScale3D should be considered relative to the world, rather than the parent

- `always_persist_rendering_state` (bool): [Read-Write] Whether to persist the rendering state even if bCaptureEveryFrame==false. This allows velocities for Motion Blur and Temporal AA to be computed.

- `asset_user_data` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `asset_user_data_editor_only` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `auto_activate` (bool): [Read-Write] Whether the component is activated at creation or must be explicitly activated.

- `auto_calculate_ortho_planes` (bool): [Read-Write] Automatically determine a min/max Near/Far clip plane position depending on OrthoWidth value

- `auto_plane_shift` (float): [Read-Write] Manually adjusts the planes of this camera, maintaining the distance between them. Positive moves out to the farplane, negative towards the near plane

- `camera_cut_this_frame` (bool): [Read-Write] True if we did a camera cut this frame. Automatically reset to false at every capture.
This flag affects various things in the renderer (such as whether to use the occlusion queries from last frame, and motion blur).
Similar to UPlayerCameraManager::bGameCameraCutThisFrame.

- `can_ever_affect_navigation` (bool): [Read-Write] Whether this component can potentially influence navigation

- `capture_every_frame` (bool): [Read-Write] Whether to update the capture’s contents every frame. If disabled, the component will render once on load and then only when moved.

- `capture_gpu_next_render` (bool): [Read-Write] Capture a GPU frame for this scene capture, next time it renders (capture program must be connected).

- `capture_on_movement` (bool): [Read-Write] Whether to update the capture’s contents on movement. Disable if you are going to capture manually from blueprint.

- `capture_sort_priority` (int32): [Read-Write] Capture priority within the frame to sort scene capture on GPU to resolve interdependencies between multiple capture components. Highest come first.

- `capture_source` (SceneCaptureSource): [Read-Write]

- `clip_plane_base` (Vector): [Read-Write] Base position for the clip plane, can be any position on the plane.

- `clip_plane_normal` (Vector): [Read-Write] Normal for the plane.

- `collection_transform` (MaterialParameterCollection): [Read-Write] Store WorldToLocal and/or Projection matrices (2D capture only) to a Material Parameter Collection on render.

- `collection_transform_projection` (Name): [Read-Write] Parameter name of the first element of the transform in the CollectionTransform Material Parameter Collection set above. Requires space for 4 vectors.

- `collection_transform_world_to_local` (Name): [Read-Write] Parameter name of the first element of the transform in the CollectionTransform Material Parameter Collection set above. Requires space for 5 vectors (large world coordinate transform).

- `component_tags` (Array[Name]): [Read-Write] Array of tags that can be used for grouping and categorizing. Can also be accessed from scripting.

- `composite_mode` (SceneCaptureCompositeMode): [Read-Write] When enabled, the scene capture will composite into the render target instead of overwriting its contents.

- `consider_unrendered_opaque_pixel_as_fully_translucent` (bool): [Read-Write] Whether to only render exponential height fog on opaque pixels which were rendered by the scene capture.

- `custom_near_clipping_plane` (float): [Read-Write] Set bOverride\_CustomNearClippingPlane to true if you want to use a custom clipping plane instead of GNearClippingPlane.

- `custom_projection_matrix` (Matrix): [Read-Write] The custom projection matrix to use

- `detail_mode` (DetailMode): [Read-Write] Set the required detail level of this component.
It will be deleted or made invisible if the world’s detail level is higher, based on platform and scalability settings.
For example, a detail mode of High may prevent this component from loading on mobile platforms.

- `dump_gpu_next_render` (bool): [Read-Write] Run DumpGPU for this scene capture, next time it renders.

- `editable_when_inherited` (bool): [Read-Write] True if this component can be modified when it was inherited from a parent actor class

- `enable_clip_plane` (bool): [Read-Write] Enables a clip plane while rendering the scene capture which is useful for portals.
The global clip plane must be enabled in the renderer project settings for this to work.

- `enable_first_person_field_of_view` (bool): [Read-Write] True if the first person field of view should be used for primitives tagged as FirstPerson.

- `enable_first_person_scale` (bool): [Read-Write] True if the first person scale should be used for primitives tagged as FirstPerson.

- `enable_orthographic_tiling` (bool): [Read-Write] Render the scene in n frames (i.e TileCount) - Ignored in Perspective mode, works only in Orthographic mode when CaptureSource uses SceneColor (not FinalColor)
If CaptureSource uses FinalColor, tiling will be ignored and a Warning message will be logged

- `exclude_from_scene_texture_extents` (bool): [Read-Write] Whether this capture should be excluded from tracking scene texture extents. This should be set when this capture is not expected to be
frequently used, especially if the capture resolution is very large. Setting this for a single-use capture will avoid influencing other
scene texture extent decisions and avoid a possible ongoing increase in memory usage.

- `first_person_field_of_view` (float): [Read-Write] The horizontal field of view (in degrees) used for primitives tagged as FirstPerson.

- `first_person_scale` (float): [Read-Write] The scale to apply to primitives tagged as FirstPerson. This is used to scale down primitives towards the camera such that they are small enough not to intersect with the scene.

- `fov_angle` (float): [Read-Write] Camera field of view (in degrees).

- `hidden_actors` (Array[Actor]): [Read-Write] The actors to hide in the scene capture.

- `hidden_in_game` (bool): [Read-Write] Whether to hide the primitive in game, if the primitive is Visible.

- `ignore_screen_percentage` (bool): [Read-Write] When rendering with main view resolution, ignore screen percentage scale and render at full resolution. Temporal AA jitter is also disabled.

- `inherit_main_view_camera_post_process_settings` (bool): [Read-Write] Inherit the main view camera post-process settings and ignore local default values. Local active overrides will function as usual.

- `is_editor_only` (bool): [Read-Write] If true, the component will be excluded from non-editor builds

- `lod_distance_factor` (float): [Read-Write] Scales the distance used by LOD. Set to values greater than 1 to cause the scene capture to use lower LODs than the main view to speed up the scene capture pass.

- `main_view_camera` (bool): [Read-Write] Render with main view camera. Enables Main View Family and Resolution. Temporal AA jitter is matched with main view.

- `main_view_family` (bool): [Read-Write] Render with main view family, for example with the main editor or game viewport which mark their view families as “main”.

- `main_view_resolution` (bool): [Read-Write] Render with main view resolution, ignoring the dimensions in the resource. Enables Main View Family.

- `main_view_resolution_divisor` (IntPoint): [Read-Write] Divisor when rendering at Main View Resolution.

- `max_view_distance_override` (float): [Read-Write] if > 0, sets a maximum render distance override. Can be used to cull distant objects from a reflection if the reflecting plane is in an enclosed area like a hallway or room

- `mobility` (ComponentMobility): [Read-Write] How often this component is allowed to move, used to make various optimizations. Only safe to set in constructor.

- `num_x_tiles` (int32): [Read-Write] Number of X tiles to render. Ignored in Perspective mode, works only in Orthographic mode

- `num_y_tiles` (int32): [Read-Write] Number of Y tiles to render. Ignored in Perspective mode, works only in Orthographic mode

- `on_component_activated` (ActorComponentActivatedSignature): [Read-Write] Called when the component has been activated, with parameter indicating if it was from a reset

- `on_component_deactivated` (ActorComponentDeactivateSignature): [Read-Write] Called when the component has been deactivated

- `ortho_width` (float): [Read-Write] The desired width (in world units) of the orthographic view (ignored in Perspective mode)

- `override_custom_near_clipping_plane` (bool): [Read-Write]

- `overscan` (float): [Read-Write] Amount to increase the view frustum by, from 0.0 for no increase to 1.0 for 100% increase

- `physics_volume_changed_delegate` (PhysicsVolumeChanged): [Read-Write] Delegate that will be called when PhysicsVolume has been changed \*

- `post_process_blend_weight` (float): [Read-Write] Range (0.0, 1.0) where 0 indicates no effect, 1 indicates full effect.

- `post_process_settings` (PostProcessSettings): [Read-Write]

- `primary_component_tick` (ActorComponentTickFunction): [Read-Write] Main tick function for the Component

- `primitive_render_mode` (SceneCapturePrimitiveRenderMode): [Read-Write] Controls what primitives get rendered into the scene capture.

- `profiling_event_name` (str): [Read-Write] Name of the profiling event.

- `projection_type` (CameraProjectionMode): [Read-Write]

- `relative_location` (Vector): [Read-Write] Location of the component relative to its parent

- `relative_rotation` (Rotator): [Read-Write] Rotation of the component relative to its parent

- `relative_scale3d` (Vector): [Read-Write] Non-uniform scaling of the component relative to its parent.
Note that scaling is always applied in local space (no shearing etc)

- `render_in_main_renderer` (bool): [Read-Write] Render scene capture as additional render passes of the main renderer rather than as an independent renderer. Applies to scene depth, device depth, base color, normal, and scene color modes (disables lighting and shadows).

- `replicate_using_registered_sub_object_list` (bool): [Read-Write] When true the replication system will only replicate the registered subobjects list
When false the replication system will instead call the virtual ReplicateSubObjects() function where the subobjects need to be manually replicated.

- `replicates` (bool): [Read-Write] Is this component currently replicating? Should the network code consider it for replication? Owning Actor must be replicating first!

- `should_update_physics_volume` (bool): [Read-Write] Whether or not the cached PhysicsVolume this component overlaps should be updated when the component is moved.
see: GetPhysicsVolume()

- `show_flag_settings` (Array[EngineShowFlagsSetting]): [Read-Write]

- `show_only_actors` (Array[Actor]): [Read-Write] The only actors to be rendered by this scene capture, if PrimitiveRenderMode is set to UseShowOnlyList.

- `texture_target` (TextureRenderTarget2D): [Read-Write] Output render target of the scene capture that can be read in materials.

- `unlit_viewmode` (SceneCaptureUnlitViewmode): [Read-Write] Option to enable a debug feature which outputs base color to the emissive channel when lighting is disabled via ShowFlag
or via Render In Main Renderer, which renders the capture as a Custom Render Pass. Note that the debug feature requires
development shaders to be compiled, generally only true in non-shipping builds on PC! To work in other cases, materials
should directly write to the emissive channel (or be unlit materials), rather than counting on the debug feature.

- `update_ortho_planes` (bool): [Read-Write] Adjusts the near/far planes and the view origin of the current camera automatically to avoid clipping and light artefacting

- `use_attach_parent_bound` (bool): [Read-Write] If true, this component uses its parents bounds when attached.
This can be a significant optimization with many components attached together.

- `use_camera_height_as_view_target` (bool): [Read-Write] If UpdateOrthoPlanes is enabled, this setting will use the cameras current height to compensate the distance to the general view (as a pseudo distance to view target when one isn’t present)

- `use_custom_projection_matrix` (bool): [Read-Write] Whether a custom projection matrix will be used during rendering. Use with caution. Does not currently affect culling

- `use_faux_ortho_view_pos` (bool): [Read-Write]
deprecated: 5.4 - bUseFauxOrthoViewPos has been deprecated alongside updates to Orthographic camera fixes

- `use_ray_tracing_if_enabled` (bool): [Read-Write] Whether to use ray tracing for this capture. Ray Tracing must be enabled in the project.

- `user_scene_texture_base_color` (Name): [Read-Write] Expose BaseColor as a UserSceneTexture. Requires “Render In Main Renderer”. Enables Main View Family and Resolution, disables “Ignore Screen Percentage”. Useful to get multiple outputs from a Custom Render Pass.

- `user_scene_texture_normal` (Name): [Read-Write] Expose Normal as a UserSceneTexture. Requires “Render In Main Renderer”. Enables Main View Family and Resolution, disables “Ignore Screen Percentage”. Useful to get multiple outputs from a Custom Render Pass.

- `user_scene_texture_scene_color` (Name): [Read-Write] Expose SceneColor (emissive/unlit) as a UserSceneTexture. Requires “Render In Main Renderer”. Enables Main View Family and Resolution, disables “Ignore Screen Percentage”. Useful to get multiple outputs from a Custom Render Pass.

- `view_lighting_channels` (ViewLightingChannels): [Read-Write] View / light masking support. Controls which lights should affect this view.

- `visible` (bool): [Read-Write] Whether to completely draw the primitive; if false, the primitive is not drawn, does not cast a shadow.



---

**add_or_update_blendable**( _blendable_object_, _weight=1.000000_) → `None`

Adds an Blendable (implements IBlendableInterface) to the array of Blendables (if it doesn’t exist) and update the weight

Parameters:

- **blendable\_object** ( _BlendableInterface_)

- **weight** ( _float_)



---

_property_ `auto_calculate_ortho_planes`: bool

[Read-Write] Automatically determine a min/max Near/Far clip plane position depending on OrthoWidth value

**Type:**

( bool)


---

_property_ `auto_plane_shift`: float

[Read-Write] Manually adjusts the planes of this camera, maintaining the distance between them. Positive moves out to the farplane, negative towards the near plane

**Type:**

( float)


---

_property_ `camera_cut_this_frame`: bool

[Read-Write] True if we did a camera cut this frame. Automatically reset to false at every capture.
This flag affects various things in the renderer (such as whether to use the occlusion queries from last frame, and motion blur).
Similar to UPlayerCameraManager::bGameCameraCutThisFrame.

**Type:**

( bool)


---

**capture_scene**() → `None`

Render the scene to the texture target immediately.
This should not be used if bCaptureEveryFrame is enabled, or the scene capture will render redundantly.
If r.SceneCapture.CullByDetailMode is set, nothing will happen if DetailMode is higher than r.DetailMode.


---

_property_ `clip_plane_base`: Vector

[Read-Write] Base position for the clip plane, can be any position on the plane.

**Type:**

( Vector)


---

_property_ `clip_plane_normal`: Vector

[Read-Write] Normal for the plane.

**Type:**

( Vector)


---

_property_ `composite_mode`: SceneCaptureCompositeMode

[Read-Write] When enabled, the scene capture will composite into the render target instead of overwriting its contents.

**Type:**

( SceneCaptureCompositeMode)


---

_property_ `consider_unrendered_opaque_pixel_as_fully_translucent`: bool

[Read-Write] Whether to only render exponential height fog on opaque pixels which were rendered by the scene capture.

**Type:**

( bool)


---

_property_ `custom_near_clipping_plane`: float

[Read-Write] Set bOverride\_CustomNearClippingPlane to true if you want to use a custom clipping plane instead of GNearClippingPlane.

**Type:**

( float)


---

_property_ `custom_projection_matrix`: Matrix

[Read-Write] The custom projection matrix to use

**Type:**

( Matrix)


---

_property_ `enable_clip_plane`: bool

[Read-Write] Enables a clip plane while rendering the scene capture which is useful for portals.
The global clip plane must be enabled in the renderer project settings for this to work.

**Type:**

( bool)


---

_property_ `enable_first_person_field_of_view`: bool

[Read-Write] True if the first person field of view should be used for primitives tagged as FirstPerson.

**Type:**

( bool)


---

_property_ `enable_first_person_scale`: bool

[Read-Write] True if the first person scale should be used for primitives tagged as FirstPerson.

**Type:**

( bool)


---

_property_ `enable_orthographic_tiling`: bool

[Read-Write] Render the scene in n frames (i.e TileCount) - Ignored in Perspective mode, works only in Orthographic mode when CaptureSource uses SceneColor (not FinalColor)
If CaptureSource uses FinalColor, tiling will be ignored and a Warning message will be logged

**Type:**

( bool)


---

_property_ `first_person_field_of_view`: float

[Read-Write] The horizontal field of view (in degrees) used for primitives tagged as FirstPerson.

**Type:**

( float)


---

_property_ `first_person_scale`: float

[Read-Write] The scale to apply to primitives tagged as FirstPerson. This is used to scale down primitives towards the camera such that they are small enough not to intersect with the scene.

**Type:**

( float)


---

_property_ `fov_angle`: float

[Read-Write] Camera field of view (in degrees).

**Type:**

( float)


---

_property_ `ignore_screen_percentage`: bool

[Read-Write] When rendering with main view resolution, ignore screen percentage scale and render at full resolution. Temporal AA jitter is also disabled.

**Type:**

( bool)


---

_property_ `inherit_main_view_camera_post_process_settings`: bool

[Read-Write] Inherit the main view camera post-process settings and ignore local default values. Local active overrides will function as usual.

**Type:**

( bool)


---

_property_ `main_view_camera`: bool

[Read-Write] Render with main view camera. Enables Main View Family and Resolution. Temporal AA jitter is matched with main view.

**Type:**

( bool)


---

_property_ `main_view_family`: bool

[Read-Write] Render with main view family, for example with the main editor or game viewport which mark their view families as “main”.

**Type:**

( bool)


---

_property_ `main_view_resolution`: bool

[Read-Write] Render with main view resolution, ignoring the dimensions in the resource. Enables Main View Family.

**Type:**

( bool)


---

_property_ `main_view_resolution_divisor`: IntPoint

[Read-Write] Divisor when rendering at Main View Resolution.

**Type:**

( IntPoint)


---

_property_ `num_x_tiles`: int

[Read-Write] Number of X tiles to render. Ignored in Perspective mode, works only in Orthographic mode

**Type:**

(int32)


---

_property_ `num_y_tiles`: int

[Read-Write] Number of Y tiles to render. Ignored in Perspective mode, works only in Orthographic mode

**Type:**

(int32)


---

_property_ `ortho_width`: float

[Read-Write] The desired width (in world units) of the orthographic view (ignored in Perspective mode)

**Type:**

( float)


---

_property_ `override_custom_near_clipping_plane`: bool

[Read-Write]

**Type:**

( bool)


---

_property_ `overscan`: float

[Read-Write] Amount to increase the view frustum by, from 0.0 for no increase to 1.0 for 100% increase

**Type:**

( float)


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

_property_ `projection_type`: CameraProjectionMode

[Read-Write]

**Type:**

( CameraProjectionMode)


---

**remove_blendable**( _blendable_object_) → `None`

Removes a blendable.

Parameters:

**blendable\_object** ( _BlendableInterface_)


---

_property_ `render_in_main_renderer`: bool

[Read-Write] Render scene capture as additional render passes of the main renderer rather than as an independent renderer. Applies to scene depth, device depth, base color, normal, and scene color modes (disables lighting and shadows).

**Type:**

( bool)


---

_property_ `texture_target`: TextureRenderTarget2D

[Read-Write] Output render target of the scene capture that can be read in materials.

**Type:**

( TextureRenderTarget2D)


---

_property_ `unlit_viewmode`: SceneCaptureUnlitViewmode

[Read-Write] Option to enable a debug feature which outputs base color to the emissive channel when lighting is disabled via ShowFlag
or via Render In Main Renderer, which renders the capture as a Custom Render Pass. Note that the debug feature requires
development shaders to be compiled, generally only true in non-shipping builds on PC! To work in other cases, materials
should directly write to the emissive channel (or be unlit materials), rather than counting on the debug feature.

**Type:**

( SceneCaptureUnlitViewmode)


---

**update_content**() → `None`

deprecated: ‘update\_content’ was renamed to ‘capture\_scene’.


---

_property_ `update_ortho_planes`: bool

[Read-Write] Adjusts the near/far planes and the view origin of the current camera automatically to avoid clipping and light artefacting

**Type:**

( bool)


---

_property_ `use_camera_height_as_view_target`: bool

[Read-Write] If UpdateOrthoPlanes is enabled, this setting will use the cameras current height to compensate the distance to the general view (as a pseudo distance to view target when one isn’t present)

**Type:**

( bool)


---

_property_ `use_custom_projection_matrix`: bool

[Read-Write] Whether a custom projection matrix will be used during rendering. Use with caution. Does not currently affect culling

**Type:**

( bool)


---

_property_ `use_faux_ortho_view_pos`: bool

[Read-Write]
deprecated: 5.4 - bUseFauxOrthoViewPos has been deprecated alongside updates to Orthographic camera fixes

**Type:**

( bool)


---

_property_ `user_scene_texture_base_color`: Name

[Read-Write] Expose BaseColor as a UserSceneTexture. Requires “Render In Main Renderer”. Enables Main View Family and Resolution, disables “Ignore Screen Percentage”. Useful to get multiple outputs from a Custom Render Pass.

**Type:**

( Name)


---

_property_ `user_scene_texture_normal`: Name

[Read-Write] Expose Normal as a UserSceneTexture. Requires “Render In Main Renderer”. Enables Main View Family and Resolution, disables “Ignore Screen Percentage”. Useful to get multiple outputs from a Custom Render Pass.

**Type:**

( Name)


---

_property_ `user_scene_texture_scene_color`: Name

[Read-Write] Expose SceneColor (emissive/unlit) as a UserSceneTexture. Requires “Render In Main Renderer”. Enables Main View Family and Resolution, disables “Ignore Screen Percentage”. Useful to get multiple outputs from a Custom Render Pass.

**Type:**

( Name)

### Table of Contents

- `unreal.SceneCaptureComponent2D`
  - `SceneCaptureComponent2D`
    - `SceneCaptureComponent2D.add_or_update_blendable()`
    - `SceneCaptureComponent2D.auto_calculate_ortho_planes`
    - `SceneCaptureComponent2D.auto_plane_shift`
    - `SceneCaptureComponent2D.camera_cut_this_frame`
    - `SceneCaptureComponent2D.capture_scene()`
    - `SceneCaptureComponent2D.clip_plane_base`
    - `SceneCaptureComponent2D.clip_plane_normal`
    - `SceneCaptureComponent2D.composite_mode`
    - `SceneCaptureComponent2D.consider_unrendered_opaque_pixel_as_fully_translucent`
    - `SceneCaptureComponent2D.custom_near_clipping_plane`
    - `SceneCaptureComponent2D.custom_projection_matrix`
    - `SceneCaptureComponent2D.enable_clip_plane`
    - `SceneCaptureComponent2D.enable_first_person_field_of_view`
    - `SceneCaptureComponent2D.enable_first_person_scale`
    - `SceneCaptureComponent2D.enable_orthographic_tiling`
    - `SceneCaptureComponent2D.first_person_field_of_view`
    - `SceneCaptureComponent2D.first_person_scale`
    - `SceneCaptureComponent2D.fov_angle`
    - `SceneCaptureComponent2D.ignore_screen_percentage`
    - `SceneCaptureComponent2D.inherit_main_view_camera_post_process_settings`
    - `SceneCaptureComponent2D.main_view_camera`
    - `SceneCaptureComponent2D.main_view_family`
    - `SceneCaptureComponent2D.main_view_resolution`
    - `SceneCaptureComponent2D.main_view_resolution_divisor`
    - `SceneCaptureComponent2D.num_x_tiles`
    - `SceneCaptureComponent2D.num_y_tiles`
    - `SceneCaptureComponent2D.ortho_width`
    - `SceneCaptureComponent2D.override_custom_near_clipping_plane`
    - `SceneCaptureComponent2D.overscan`
    - `SceneCaptureComponent2D.post_process_blend_weight`
    - `SceneCaptureComponent2D.post_process_settings`
    - `SceneCaptureComponent2D.projection_type`
    - `SceneCaptureComponent2D.remove_blendable()`
    - `SceneCaptureComponent2D.render_in_main_renderer`
    - `SceneCaptureComponent2D.texture_target`
    - `SceneCaptureComponent2D.unlit_viewmode`
    - `SceneCaptureComponent2D.update_content()`
    - `SceneCaptureComponent2D.update_ortho_planes`
    - `SceneCaptureComponent2D.use_camera_height_as_view_target`
    - `SceneCaptureComponent2D.use_custom_projection_matrix`
    - `SceneCaptureComponent2D.use_faux_ortho_view_pos`
    - `SceneCaptureComponent2D.user_scene_texture_base_color`
    - `SceneCaptureComponent2D.user_scene_texture_normal`
    - `SceneCaptureComponent2D.user_scene_texture_scene_color`