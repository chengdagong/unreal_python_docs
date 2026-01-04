# unreal.SplineComponent

```python
class unreal.SplineComponent(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``PrimitiveComponent``


A spline component is a spline shape which can be used for other purposes (e.g. animating objects). It contains debug rendering capabilities.
see: https://docs.unrealengine.com/latest/INT/Resources/ContentExamples/Blueprint\_Splines

**C++ Source:**

- **Module**: Engine

- **File**: SplineComponent.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `absolute_location` (bool): [Read-Write] If RelativeLocation should be considered relative to the world, rather than the parent

- `absolute_rotation` (bool): [Read-Write] If RelativeRotation should be considered relative to the world, rather than the parent

- `absolute_scale` (bool): [Read-Write] If RelativeScale3D should be considered relative to the world, rather than the parent

- `adjust_tangents_on_snap` (bool): [Read-Write] Adjust tangents after snapping.

- `affect_distance_field_lighting` (bool): [Read-Write] Controls whether the primitive should affect dynamic distance field lighting methods. This flag is only used if CastShadow is true.

- `affect_dynamic_indirect_lighting` (bool): [Read-Write] Controls whether the primitive should influence indirect lighting.

- `affect_indirect_lighting_while_hidden` (bool): [Read-Write] Controls whether the primitive should affect indirect lighting when hidden. This flag is only used if bAffectDynamicIndirectLighting is true.

- `allow_cull_distance_volume` (bool): [Read-Write] Whether to accept cull distance volumes to modify cached cull distance.

- `allow_discontinuous_spline` (bool): [Read-Write] Whether the spline’s leave and arrive tangents can be different

- `always_create_physics_state` (bool): [Read-Write] Indicates if we’d like to create physics state all the time (for collision and simulation).
If you set this to false, it still will create physics state if collision or simulation activated.
This can help performance if you’d like to avoid overhead of creating physics state when triggers

- `apply_impulse_on_damage` (bool): [Read-Write] True for damage to this component to apply physics impulse, false to opt out of these impulses.

- `asset_user_data` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `asset_user_data_editor_only` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `auto_activate` (bool): [Read-Write] Whether the component is activated at creation or must be explicitly activated.

- `body_instance` (BodyInstance): [Read-Write] Physics scene information for this component, holds a single rigid body with multiple shapes.

- `bounds_scale` (float): [Read-Write] Scales the bounds of the object.
This is useful when using World Position Offset to animate the vertices of the object outside of its bounds.
Warning: Increasing the bounds of an object will reduce performance and shadow quality!
Currently only used by StaticMeshComponent and SkeletalMeshComponent.

- `cached_max_draw_distance` (float): [Read-Only] The distance to cull this primitive at.
A CachedMaxDrawDistance of 0 indicates that the primitive should not be culled by distance.

- `can_character_step_up_on` (CanBeCharacterBase): [Read-Write] Determine whether a Character can step up onto this component.
This controls whether they can try to step up on it when they bump in to it, not whether they can walk on it after landing on it.
see: FWalkableSlopeOverride

- `can_ever_affect_navigation` (bool): [Read-Write] Whether this component can potentially influence navigation

- `cast_cinematic_shadow` (bool): [Read-Write] Whether this component should cast shadows from lights that have bCastShadowsFromCinematicObjectsOnly enabled.
This is useful for characters in a cinematic with special cinematic lights, where the cost of shadowmap rendering of the environment is undesired.

- `cast_contact_shadow` (bool): [Read-Write] Whether the object should cast contact shadows.
This flag is only used if CastShadow is true.

- `cast_dynamic_shadow` (bool): [Read-Write] Controls whether the primitive should cast shadows in the case of non precomputed shadowing. This flag is only used if CastShadow is true and if FirstPersonPrimitiveType is not set to FirstPerson.

- `cast_far_shadow` (bool): [Read-Write] When enabled, the component will be rendering into the far shadow cascades (only for directional lights). This flag is only used if CastShadow is true and if FirstPersonPrimitiveType is not set to FirstPerson.

- `cast_hidden_shadow` (bool): [Read-Write] If true, the primitive will cast shadows even if bHidden is true.
Controls whether the primitive should cast shadows when hidden.
This flag is only used if CastShadow is true and if FirstPersonPrimitiveType is not set to WorldSpaceRepresentation.

- `cast_inset_shadow` (bool): [Read-Write] Whether this component should create a per-object shadow that gives higher effective shadow resolution.
Useful for cinematic character shadowing. Assumed to be enabled if bSelfShadowOnly is enabled.

- `cast_shadow` (bool): [Read-Write] Controls whether the primitive component should cast a shadow or not.

- `cast_shadow_as_two_sided` (bool): [Read-Write] Whether this primitive should cast dynamic shadows as if it were a two sided material.

- `cast_static_shadow` (bool): [Read-Write] Whether the object should cast a static shadow from shadow casting lights. This flag is only used if CastShadow is true and if FirstPersonPrimitiveType is not set to FirstPerson.

- `cast_volumetric_translucent_shadow` (bool): [Read-Write] Whether the object should cast a volumetric translucent shadow.
Volumetric translucent shadows are useful for primitives with smoothly changing opacity like particles representing a volume,
but have artifacts when used on highly opaque surfaces. This flag is only used if CastShadow is true and if FirstPersonPrimitiveType is not set to FirstPerson.

- `closed_loop` (bool): [Read-Write] Whether the spline is to be considered as a closed loop.
Use SetClosedLoop() to set this property, and IsClosedLoop() to read it.

- `component_tags` (Array[Name]): [Read-Write] Array of tags that can be used for grouping and categorizing. Can also be accessed from scripting.

- `consider_for_actor_placement_when_hidden` (bool): [Read-Write] If true, this component will be considered for placement when dragging and placing items in the editor even if it is not visible, such as in the case of hidden collision meshes

- `custom_depth_stencil_value` (int32): [Read-Write] Optionally write this 0-255 value to the stencil buffer in CustomDepth pass (Requires project setting or r.CustomDepth == 3)

- `custom_depth_stencil_write_mask` (RendererStencilMask): [Read-Write] Mask used for stencil buffer writes.

- `custom_primitive_data` (CustomPrimitiveData): [Read-Write] Optional user defined default values for the custom primitive data of this primitive

- `default_up_vector` (Vector): [Read-Write] Default up vector in local space to be used when calculating transforms along the spline

- `detail_mode` (DetailMode): [Read-Write] Set the required detail level of this component.
It will be deleted or made invisible if the world’s detail level is higher, based on platform and scalability settings.
For example, a detail mode of High may prevent this component from loading on mobile platforms.

- `draw_debug` (bool): [Read-Write] If true, the spline will be rendered if the Splines showflag is set.

- `duration` (float): [Read-Write] Specifies the duration of the spline in seconds

- `editable_when_inherited` (bool): [Read-Write] True if this component can be modified when it was inherited from a parent actor class

- `editor_selected_spline_segment_color` (LinearColor): [Read-Write] Color of selected spline component parts in the editor

- `editor_tangent_color` (LinearColor): [Read-Write] Color of spline point tangents in the editor

- `editor_unselected_spline_segment_color` (LinearColor): [Read-Write] Color of unselected spline component parts in the editor

- `emissive_light_source` (bool): [Read-Write] Whether the primitive will be used as an emissive light source.

- `enable_auto_lod_generation` (bool): [Read-Write] Whether to include this component in HLODs or not.

- `exclude_for_specific_hlod_levels` (Array[int32]): [Read-Write]
deprecated: WARNING: This property has been deprecated, use the SetExcludedFromHLODLevel/IsExcludedFromHLODLevel functions instead

- `exclude_from_hlod_levels` (uint8): [Read-Write] Which specific HLOD levels this component should be excluded from

- `exclude_from_light_attachment_group` (bool): [Read-Write] If set, then it overrides any bLightAttachmentsAsGroup set in a parent.

- `fill_collision_underneath_for_navmesh` (bool): [Read-Write] If set, navmesh will not be generated under the surface of the geometry

- `first_person_primitive_type` (FirstPersonPrimitiveType): [Read-Write] If this is set to FirstPerson, the camera FirstPersonFieldOfView and FirstPersonScale parameters will be used on this component. These parameters can be used to render the component with a different field of view and a smaller depth range such that clipping with the scene can be avoided. This is useful for rendering first person view geometry.

- `force_mip_streaming` (bool): [Read-Write] If true, forces mips for textures used by this component to be resident when this component’s level is loaded.

- `generate_overlap_events` (bool): [Read-Write]

- `has_per_instance_hit_proxies` (bool): [Read-Write] If true a hit-proxy will be generated for each instance of instanced static meshes.
This allows for other systems, like selection in viewports, to function at the individual instance.

- `hidden_in_game` (bool): [Read-Write] Whether to hide the primitive in game, if the primitive is Visible.

- `hidden_in_scene_capture` (bool): [Read-Write] When true, will not be captured by Scene Capture

- `hlod_batching_policy` (HLODBatchingPolicy): [Read-Write] Determines how the geometry of a component will be incorporated in proxy (simplified) HLODs.

- `holdout` (bool): [Read-Write] If this is True, this primitive will render black with an alpha of 0, but all secondary effects (shadows, reflections, indirect lighting) remain. This feature requires activating the project setting(s) “Alpha Output”, and “Support Primitive Alpha Holdout” if using the deferred renderer.

- `ignore_radial_force` (bool): [Read-Write] Will ignore radial forces applied to this component.

- `ignore_radial_impulse` (bool): [Read-Write] Will ignore radial impulses applied to this component.

- `indirect_lighting_cache_quality` (IndirectLightingCacheQuality): [Read-Write] Quality of indirect lighting for Movable primitives. This has a large effect on Indirect Lighting Cache update time.

- `input_spline_points_to_construction_script` (bool): [Read-Write] Whether the spline points should be passed to the User Construction Script so they can be further manipulated by it.
If false, they will not be visible to it, and it will not be able to influence the per-instance positions set in the editor.

- `is_editor_only` (bool): [Read-Write] If true, the component will be excluded from non-editor builds

- `ld_max_draw_distance` (float): [Read-Write] Max draw distance exposed to LDs. The real max draw distance is the min (disregarding 0) of this and volumes affecting this object.

- `light_attachments_as_group` (bool): [Read-Write] Whether to light this component and any attachments as a group. This only has effect on the root component of an attachment tree.
When enabled, attached component shadowing settings like bCastInsetShadow, bCastVolumetricTranslucentShadow, etc, will be ignored.
This is useful for improving performance when multiple movable components are attached together.

- `lighting_channels` (LightingChannels): [Read-Write] Channels that this component should be in. Lights with matching channels will affect the component.
These channels only apply to opaque materials, direct lighting, and dynamic lighting and shadowing.
Lighting channels are only supported on translucent materials using forward shading (i.e. when not using the translucency lighting volume).

- `lightmap_type` (LightmapType): [Read-Write]

- `loop_position` (float): [Read-Write]

- `loop_position_override` (bool): [Read-Write]

- `min_draw_distance` (float): [Read-Write] The minimum distance at which the primitive should be rendered,
measured in world space units from the center of the primitive’s bounding sphere to the camera position.

- `mobility` (ComponentMobility): [Read-Write] How often this component is allowed to move, used to make various optimizations. Only safe to set in constructor.

- `multi_body_overlap` (bool): [Read-Write] If true, this component will generate individual overlaps for each overlapping physics body if it is a multi-body component. When false, this component will
generate only one overlap, regardless of how many physics bodies it has and how many of them are overlapping another component/body. This flag has no
influence on single body components.

- `never_distance_cull` (bool): [Read-Write] When enabled this object will not be culled by distance. This is ignored if a child of a HLOD.

- `on_begin_cursor_over` (ComponentBeginCursorOverSignature): [Read-Write] Event called when the mouse cursor is moved over this component and mouse over events are enabled in the player controller

- `on_clicked` (ComponentOnClickedSignature): [Read-Write] Event called when the left mouse button is clicked while the mouse is over this component and click events are enabled in the player controller

- `on_component_activated` (ActorComponentActivatedSignature): [Read-Write] Called when the component has been activated, with parameter indicating if it was from a reset

- `on_component_begin_overlap` (ComponentBeginOverlapSignature): [Read-Write] Event called when something starts to overlaps this component, for example a player walking into a trigger.
For events when objects have a blocking collision, for example a player hitting a wall, see ‘Hit’ events.
note: Both this component and the other one must have GetGenerateOverlapEvents() set to true to generate overlap events.
note: When receiving an overlap from another object’s movement, the directions of ‘Hit.Normal’ and ‘Hit.ImpactNormal’ will be adjusted to indicate force from the other object against this object.

- `on_component_deactivated` (ActorComponentDeactivateSignature): [Read-Write] Called when the component has been deactivated

- `on_component_end_overlap` (ComponentEndOverlapSignature): [Read-Write] Event called when something stops overlapping this component
note: Both this component and the other one must have GetGenerateOverlapEvents() set to true to generate overlap events.

- `on_component_hit` (ComponentHitSignature): [Read-Write] Event called when a component hits (or is hit by) something solid. This could happen due to things like Character movement, using Set Location with ‘sweep’ enabled, or physics simulation.
For events when objects overlap (e.g. walking into a trigger) see the ‘Overlap’ event.
note: For collisions during physics simulation to generate hit events, ‘Simulation Generates Hit Events’ must be enabled for this component.
note: When receiving a hit from another object’s movement, the directions of ‘Hit.Normal’ and ‘Hit.ImpactNormal’ will be adjusted to indicate force from the other object against this object.
note: NormalImpulse will be filled in for physics-simulating bodies, but will be zero for swept-component blocking collisions.

- `on_component_physics_state_changed` (ComponentPhysicsStateChanged): [Read-Write] Event called when physics state is created or destroyed for this component

- `on_component_sleep` (ComponentSleepSignature): [Read-Write] Event called when the underlying physics objects is put to sleep

- `on_component_wake` (ComponentWakeSignature): [Read-Write] Event called when the underlying physics objects is woken up

- `on_end_cursor_over` (ComponentEndCursorOverSignature): [Read-Write] Event called when the mouse cursor is moved off this component and mouse over events are enabled in the player controller

- `on_input_touch_begin` (ComponentOnInputTouchBeginSignature): [Read-Write] Event called when a touch input is received over this component when touch events are enabled in the player controller

- `on_input_touch_end` (ComponentOnInputTouchEndSignature): [Read-Write] Event called when a touch input is released over this component when touch events are enabled in the player controller

- `on_input_touch_enter` (ComponentBeginTouchOverSignature): [Read-Write] Event called when a finger is moved over this component when touch over events are enabled in the player controller

- `on_input_touch_leave` (ComponentEndTouchOverSignature): [Read-Write] Event called when a finger is moved off this component when touch over events are enabled in the player controller

- `on_released` (ComponentOnReleasedSignature): [Read-Write] Event called when the left mouse button is released while the mouse is over this component click events are enabled in the player controller

- `only_owner_see` (bool): [Read-Write] If this is True, this component will only be visible when the view actor is the component’s owner, directly or indirectly.

- `owner_no_see` (bool): [Read-Write] If this is True, this component won’t be visible when the view actor is the component’s owner, directly or indirectly. Will be internally set to true when FirstPersonPrimitiveType is set to WorldSpaceRepresentation.

- `physics_volume_changed_delegate` (PhysicsVolumeChanged): [Read-Write] Delegate that will be called when PhysicsVolume has been changed \*

- `primary_component_tick` (ActorComponentTickFunction): [Read-Write] Main tick function for the Component

- `rasterize_as_filled_convex_volume` (bool): [Read-Write] If set, the geometry gathered for navigation data generation will be converted into a filled vertical convex volume.
It means that all collision geometries of the asset are merged vertically resulting in a grid of vertical columns that encompass the asset.
This can be useful to represent the interior of the surface and prevent navmesh inside.

- `ray_tracing_group_culling_priority` (RayTracingGroupCullingPriority): [Read-Write] Defines how quickly it should be culled. For example buildings should have a low priority, but small dressing should have a high priority.

- `ray_tracing_group_id` (int32): [Read-Write] Defines run-time groups of components. For example allows to assemble multiple parts of a building at runtime.
  -1 means that component doesn’t belong to any group.

- `receive_mobile_csm_shadows` (bool): [Read-Write] Mobile only:
If disabled this component will not receive CSM shadows. (Components that do not receive CSM may have reduced shading cost)

- `receives_decals` (bool): [Read-Write] Whether the primitive receives decals.

- `relative_location` (Vector): [Read-Write] Location of the component relative to its parent

- `relative_rotation` (Rotator): [Read-Write] Rotation of the component relative to its parent

- `relative_scale3d` (Vector): [Read-Write] Non-uniform scaling of the component relative to its parent.
Note that scaling is always applied in local space (no shearing etc)

- `render_custom_depth` (bool): [Read-Write] If true, this component will be rendered in the CustomDepth pass (usually used for outlines)

- `render_in_depth_pass` (bool): [Read-Write] If true, this component will be rendered in the depth pass even if it’s not rendered in the main pass

- `render_in_main_pass` (bool): [Read-Write] If true, this component will be rendered in the main pass (z prepass, basepass, transparency)

- `reparam_steps_per_segment` (int32): [Read-Write] Number of steps per spline segment to place in the reparameterization table

- `replicate_physics_to_autonomous_proxy` (bool): [Read-Write] True if physics should be replicated to autonomous proxies. This should be true for

server-authoritative simulations, and false for client authoritative simulations.

- `replicate_using_registered_sub_object_list` (bool): [Read-Write] When true the replication system will only replicate the registered subobjects list
When false the replication system will instead call the virtual ReplicateSubObjects() function where the subobjects need to be manually replicated.

- `replicates` (bool): [Read-Write] Is this component currently replicating? Should the network code consider it for replication? Owning Actor must be replicating first!

- `return_material_on_move` (bool): [Read-Write] If true, component sweeps will return the material in their hit result.
see: MoveComponent(), FHitResult

- `runtime_virtual_textures` (Array[RuntimeVirtualTexture]): [Read-Write] Array of runtime virtual textures into which we draw the mesh for this actor.
The material also needs to be set up to output to a virtual texture.

- `scale_visualization_width` (float): [Read-Write] Width of spline in editor for use with scale visualization

- `self_shadow_only` (bool): [Read-Write] When enabled, the component will only cast a shadow on itself and not other components in the world.
This is especially useful for first person weapons, and forces bCastInsetShadow to be enabled.

- `shadow_cache_invalidation_behavior` (ShadowCacheInvalidationBehavior): [Read-Write] Control shadow invalidation behavior, in particular with respect to Virtual Shadow Maps and material effects like World Position Offset.

- `should_update_physics_volume` (bool): [Read-Write] Whether or not the cached PhysicsVolume this component overlaps should be updated when the component is moved.
see: GetPhysicsVolume()

- `should_visualize_scale` (bool): [Read-Write] Whether scale visualization should be displayed

- `single_sample_shadow_from_stationary_lights` (bool): [Read-Write] Whether the whole component should be shadowed as one from stationary lights, which makes shadow receiving much cheaper.
When enabled shadowing data comes from the volume lighting samples precomputed by Lightmass, which are very sparse.
This is currently only used on stationary directional lights.

- `spline` (Spline): [Read-Write]

- `spline_curves` (SplineCurves): [Read-Write]

- `spline_has_been_edited` (bool): [Read-Write] Whether the spline has been edited from its default by the spline component visualizer

- `static_when_not_moveable` (bool): [Read-Write] When false, the underlying physics body will contain all sim data (mass, inertia tensor, etc) even if mobility is not set to Moveable

- `stationary_endpoints` (bool): [Read-Write] Whether the endpoints of the spline are considered stationary when traversing the spline at non-constant velocity. Essentially this sets the endpoints’ tangents to zero vectors.

- `trace_complex_on_move` (bool): [Read-Write] If true, component sweeps with this component should trace against complex collision during movement (for example, each triangle of a mesh).
If false, collision will be resolved against simple collision bounds instead.
see: MoveComponent()

- `translucency_sort_distance_offset` (float): [Read-Write] Modified sort distance offset for translucent objects in world units.
A positive number will move the sort distance further and a negative number will move the distance closer.

Ignored if the object is not translucent.
Warning: Adjusting this value will prevent the renderer from correctly sorting based on distance. Only modify this value if you are certain it will not cause visual artifacts.

- `translucency_sort_priority` (int32): [Read-Write] Translucent objects with a lower sort priority draw behind objects with a higher priority.
Translucent objects with the same priority are rendered from back-to-front based on their bounds origin.
This setting is also used to sort objects being drawn into a runtime virtual texture.

Ignored if the object is not translucent. The default priority is zero.
Warning: This should never be set to a non-default value unless you know what you are doing, as it will prevent the renderer from sorting correctly.
It is especially problematic on dynamic gameplay effects.

- `treat_as_background_for_occlusion` (bool): [Read-Write] Treat this primitive as part of the background for occlusion purposes. This can be used as an optimization to reduce the cost of rendering skyboxes, large ground planes that are part of the vista, etc.

- `use_as_occluder` (bool): [Read-Write] Whether to render the primitive in the depth only pass.
This should generally be true for all objects, and let the renderer make decisions about whether to render objects in the depth only pass.
todo: if any rendering features rely on a complete depth only pass, this variable needs to go away.

- `use_attach_parent_bound` (bool): [Read-Write] If true, this component uses its parents bounds when attached.
This can be a significant optimization with many components attached together.

- `virtual_texture_cull_mips` (int8): [Read-Write] Number of lower mips in the runtime virtual texture to skip for rendering this primitive.
Larger values reduce the effective draw distance in the runtime virtual texture.
This culling method doesn’t take into account primitive size or virtual texture size.

- `virtual_texture_lod_bias` (int8): [Read-Write] Bias to the LOD selected for rendering to runtime virtual textures.

- `virtual_texture_min_coverage` (int8): [Read-Write] Set the minimum pixel coverage before culling from the runtime virtual texture.
Larger values reduce the effective draw distance in the runtime virtual texture.

- `virtual_texture_render_pass_type` (RuntimeVirtualTextureMainPassType): [Read-Write] Controls if this component draws in the main pass as well as in the virtual texture.

- `visible` (bool): [Read-Write] Whether to completely draw the primitive; if false, the primitive is not drawn, does not cast a shadow.

- `visible_in_ray_tracing` (bool): [Read-Write] If true, this component will be visible in ray tracing effects. Turning this off will remove it from ray traced reflections, shadows, etc.

- `visible_in_real_time_sky_captures` (bool): [Read-Write] If true, this component will be visible in real-time sky light reflection captures.

- `visible_in_reflection_captures` (bool): [Read-Write] If true, this component will be visible in reflection captures.

- `visible_in_scene_capture_only` (bool): [Read-Write] When true, will only be visible in Scene Capture



---

**add_point**( _point_, _update_spline=True_) → `None`

Adds an FSplinePoint to the spline. This contains its input key, position, tangent, rotation and scale.

Parameters:

- **point** ( _SplinePoint_)

- **update\_spline** ( _bool_)



---

**add_points**( _points_, _update_spline=True_) → `None`

Adds an array of FSplinePoints to the spline.

Parameters:

- **points** ( _Array_ _\_ [_SplinePoint_ _]_)

- **update\_spline** ( _bool_)



---

**add_spline_local_point**( _position_) → `None`

Adds a local space point to the spline
deprecated: Please use AddSplinePoint, specifying SplineCoordinateSpace::Local

Parameters:

**position** ( _Vector_)


---

**add_spline_point**( _position_, _coordinate_space_, _update_spline=True_) → `None`

Adds a point to the spline

Parameters:

- **position** ( _Vector_)

- **coordinate\_space** ( _SplineCoordinateSpace_)

- **update\_spline** ( _bool_)



---

**add_spline_point_at_index**( _position_, _index_, _coordinate_space_, _update_spline=True_) → `None`

Adds a point to the spline at the specified index

Parameters:

- **position** ( _Vector_)

- **index** ( _int32_)

- **coordinate\_space** ( _SplineCoordinateSpace_)

- **update\_spline** ( _bool_)



---

**add_spline_world_point**( _position_) → `None`

Adds a world space point to the spline
deprecated: Please use AddSplinePoint, specifying SplineCoordinateSpace::World

Parameters:

**position** ( _Vector_)


---

_property_ `b_always_render_in_editor`: bool

‘b\_always\_render\_in\_editor’ was renamed to ‘draw\_debug’.

**Type:**

deprecated


---

**clear_spline_points**( _update_spline=True_) → `None`

Clears all the points in the spline

Parameters:

**update\_spline** ( _bool_)


---

**convert_spline_segment_to_poly_line**( _spline_point_start_index_, _coordinate_space_, _max_square_distance_from_spline_) → `Array[Vector]orNone`

Given a threshold, returns a list of vertices along the spline segment that, treated as a list of segments (polyline), matches the spline shape.

Parameters:

- **spline\_point\_start\_index** ( _int32_)

- **coordinate\_space** ( _SplineCoordinateSpace_)

- **max\_square\_distance\_from\_spline** ( _float_)


Returns:

out\_points (Array[Vector]):

Return type:

Array\ [Vector] or None


---

**convert_spline_to_poly_line**( _coordinate_space_, _max_square_distance_from_spline_) → `Array[Vector]orNone`

Given a threshold, returns a list of vertices along the spline that, treated as a list of segments (polyline), matches the spline shape.

Parameters:

- **coordinate\_space** ( _SplineCoordinateSpace_)

- **max\_square\_distance\_from\_spline** ( _float_)


Returns:

out\_points (Array[Vector]):

Return type:

Array\ [Vector] or None


---

**convert_spline_to_poly_line_with_distances**( _coordinate_space_, _max_square_distance_from_spline_) → `(out_points=Array[Vector],out_distances_along_spline=Array[double])orNone`

Given a threshold, returns a list of vertices along the spline that, treated as a list of segments (polyline), matches the spline shape. Also fills a list of corresponding distances along the spline for each point.

Parameters:

- **coordinate\_space** ( _SplineCoordinateSpace_)

- **max\_square\_distance\_from\_spline** ( _float_)


Returns:

out\_points (Array[Vector]):

out\_distances\_along\_spline (Array[double]):

Return type:

tuple or None


---

**convert_spline_to_polyline_in_distance_range**( _coordinate_space_, _max_square_distance_from_spline_, _start_dist_along_spline_, _end_dist_along_spline_, _allow_wrapping_if_closed=True_) → `(out_points=Array[Vector],out_distances_along_spline=Array[double])orNone`

Given a threshold and a start and end distance range, returns a list of vertices along the spline that, treated as a list of segments (polyline), matches the spline shape in that range. Also fills a list of corresponding distances along the spline for each point.

Parameters:

- **coordinate\_space** ( _SplineCoordinateSpace_)

- **max\_square\_distance\_from\_spline** ( _float_)

- **start\_dist\_along\_spline** ( _float_)

- **end\_dist\_along\_spline** ( _float_)

- **allow\_wrapping\_if\_closed** ( _bool_)


Returns:

out\_points (Array[Vector]):

out\_distances\_along\_spline (Array[double]):

Return type:

tuple or None


---

**convert_spline_to_polyline_in_time_range**( _coordinate_space_, _max_square_distance_from_spline_, _start_time_along_spline_, _end_time_along_spline_, _use_constant_velocity_, _allow_wrapping_if_closed=True_) → `(out_points=Array[Vector],out_distances_along_spline=Array[double])orNone`

Given a threshold and start and end time range, returns a list of vertices along the spline that, treated as a list of segments (polyline), matches the spline shape in that range. Also fills a list of corresponding distances along the spline for each point.

Parameters:

- **coordinate\_space** ( _SplineCoordinateSpace_)

- **max\_square\_distance\_from\_spline** ( _float_)

- **start\_time\_along\_spline** ( _float_)

- **end\_time\_along\_spline** ( _float_)

- **use\_constant\_velocity** ( _bool_)

- **allow\_wrapping\_if\_closed** ( _bool_)


Returns:

out\_points (Array[Vector]):

out\_distances\_along\_spline (Array[double]):

Return type:

tuple or None


---

**create_float_property_channel**( _property_name_) → `None`

Create a float attribute channel.

Parameters:

**property\_name** ( _Name_) – The desired name of the new attribute channel.


---

_property_ `default_up_vector`: Vector

[Read-Write] Default up vector in local space to be used when calculating transforms along the spline

**Type:**

( Vector)


---

**divide_spline_into_polyline_recursive**( _start_distance_along_spline_, _end_distance_along_spline_, _coordinate_space_, _max_square_distance_from_spline_) → `Array[Vector]orNone`

Given a threshold, recursively sub-divides the spline section until the list of segments (polyline) matches the spline shape. Note: Prefer ConvertSplineToPolyline\_InDistanceRange

Parameters:

- **start\_distance\_along\_spline** ( _float_)

- **end\_distance\_along\_spline** ( _float_)

- **coordinate\_space** ( _SplineCoordinateSpace_)

- **max\_square\_distance\_from\_spline** ( _float_)


Returns:

out\_points (Array[Vector]):

Return type:

Array\ [Vector] or None


---

**divide_spline_into_polyline_recursive_with_distances**( _start_distance_along_spline_, _end_distance_along_spline_, _coordinate_space_, _max_square_distance_from_spline_) → `(out_points=Array[Vector],out_distances_along_spline=Array[double])orNone`

Given a threshold, recursively sub-divides the spline section until the list of segments (polyline) matches the spline shape. Note: Prefer ConvertSplineToPolyline\_InDistanceRange

Parameters:

- **start\_distance\_along\_spline** ( _float_)

- **end\_distance\_along\_spline** ( _float_)

- **coordinate\_space** ( _SplineCoordinateSpace_)

- **max\_square\_distance\_from\_spline** ( _float_)


Returns:

out\_points (Array[Vector]):

out\_distances\_along\_spline (Array[double]):

Return type:

tuple or None


---

_property_ `draw_debug`: bool

[Read-Write] If true, the spline will be rendered if the Splines showflag is set.

**Type:**

( bool)


---

_property_ `duration`: float

[Read-Write] Specifies the duration of the spline in seconds

**Type:**

( float)


---

**find_direction_closest_to_world_location**( _world_location_, _coordinate_space_) → `Vector`

Given a location, in world space, return a unit direction vector of the spline tangent closest to the location.

Parameters:

- **world\_location** ( _Vector_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

Vector


---

**find_input_key_closest_to_world_location**( _world_location_) → `float`

Given a location, in world space, return the input key closest to that location.

Parameters:

**world\_location** ( _Vector_)

Return type:

float


---

**find_input_key_on_segment_closest_to_world_location**( _world_location_, _index_) → `float`

Given a location, in world space, return the input key closest to that location on the specified segment.

Parameters:

- **world\_location** ( _Vector_)

- **index** ( _int32_)


Return type:

float


---

**find_location_closest_to_world_location**( _world_location_, _coordinate_space_) → `Vector`

Given a location, in world space, return the point on the curve that is closest to the location.

Parameters:

- **world\_location** ( _Vector_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

Vector


---

**find_right_vector_closest_to_world_location**( _world_location_, _coordinate_space_) → `Vector`

Given a location, in world space, return a unit direction vector corresponding to the spline’s right vector closest to the location.

Parameters:

- **world\_location** ( _Vector_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

Vector


---

**find_roll_closest_to_world_location**( _world_location_, _coordinate_space_) → `float`

Given a location, in world space, return the spline’s roll closest to the location, in degrees.

Parameters:

- **world\_location** ( _Vector_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

float


---

**find_rotation_closest_to_world_location**( _world_location_, _coordinate_space_) → `Rotator`

Given a location, in world space, return rotation corresponding to the spline’s rotation closest to the location.

Parameters:

- **world\_location** ( _Vector_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

Rotator


---

**find_scale_closest_to_world_location**( _world_location_) → `Vector`

Given a location, in world space, return the spline’s scale closest to the location.

Parameters:

**world\_location** ( _Vector_)

Return type:

Vector


---

**find_tangent_closest_to_world_location**( _world_location_, _coordinate_space_) → `Vector`

Given a location, in world space, return the tangent vector of the spline closest to the location.

Parameters:

- **world\_location** ( _Vector_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

Vector


---

**find_transform_closest_to_world_location**( _world_location_, _coordinate_space_, _use_scale=False_) → `Transform`

Given a location, in world space, return an FTransform closest to that location.

Parameters:

- **world\_location** ( _Vector_)

- **coordinate\_space** ( _SplineCoordinateSpace_)

- **use\_scale** ( _bool_)


Return type:

Transform


---

**find_up_vector_closest_to_world_location**( _world_location_, _coordinate_space_) → `Vector`

Given a location, in world space, return a unit direction vector corresponding to the spline’s up vector closest to the location.

Parameters:

- **world\_location** ( _Vector_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

Vector


---

**get_arrive_tangent_at_spline_point**( _point_index_, _coordinate_space_) → `Vector`

Get the arrive tangent at spline point

Parameters:

- **point\_index** ( _int32_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

Vector


---

**get_default_up_vector**( _coordinate_space_) → `Vector`

Gets the default up vector used by this spline

Parameters:

**coordinate\_space** ( _SplineCoordinateSpace_)

Return type:

Vector


---

**get_direction_at_distance_along_spline**( _distance_, _coordinate_space_) → `Vector`

Given a distance along the length of this spline, return a unit direction vector of the spline tangent there.

Parameters:

- **distance** ( _float_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

Vector


---

**get_direction_at_spline_input_key**( _key_, _coordinate_space_) → `Vector`

Get unit direction along spline at the provided input key value

Parameters:

- **key** ( _float_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

Vector


---

**get_direction_at_spline_point**( _point_index_, _coordinate_space_) → `Vector`

Get the direction at spline point

Parameters:

- **point\_index** ( _int32_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

Vector


---

**get_direction_at_time**( _time_, _coordinate_space_, _use_constant_velocity=False_) → `Vector`

Given a time from 0 to the spline duration, return a unit direction vector of the spline tangent there.

Parameters:

- **time** ( _float_)

- **coordinate\_space** ( _SplineCoordinateSpace_)

- **use\_constant\_velocity** ( _bool_)


Return type:

Vector


---

**get_distance_along_spline_at_location**( _location_, _coordinate_space_) → `float`

Get distance along the spline at closest point of the provided input location

Parameters:

- **location** ( _Vector_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

float


---

**get_distance_along_spline_at_spline_input_key**( _key_) → `float`

Get distance along the spline at the provided input key value

Parameters:

**key** ( _float_)

Return type:

float


---

**get_distance_along_spline_at_spline_point**( _point_index_) → `float`

Get the distance along the spline at the spline point

Parameters:

**point\_index** ( _int32_)

Return type:

float


---

**get_float_property_at_index**( _index_, _property_name_) → `float`

Get a float attribute value by index.

Parameters:

- **index** ( _int32_) – The index of the specified attribute.

- **property\_name** ( _Name_) – The name of the attribute channel containing the specified attribute.


Returns:

The attribute value.

Return type:

float


---

**get_float_property_at_spline_input_key**( _key_, _property_name_) → `float`

Get a float attribute value by parameter.

Parameters:

- **key** ( _float_) – The parameter to use when evaluating the specified attribute channel.

- **property\_name** ( _Name_) – The name of the attribute channel to evaluate.


Returns:

The attribute value.

Return type:

float


---

**get_float_property_at_spline_point**( _index_, _property_name_) → `float`

Get a metadata property float value along the spline at spline point

Parameters:

- **index** ( _int32_)

- **property\_name** ( _Name_)


Return type:

float


---

**get_float_property_channels**() → `Array\ [Name]Returns:`

An array of all float attribute channel names.

Return type:

Array\ [Name]


---

**get_float_property_input_key_at_index**( _index_, _property_name_) → `float`

Get a float attribute parameter by index.

Parameters:

- **index** ( _int32_) – The index of the specified attribute.

- **property\_name** ( _Name_) – The name of the attribute channel containing the specified attribute.


Returns:

The attribute parameter.

Return type:

float


---

**get_input_key_at_distance_along_spline**( _distance_) → `float`

This method has been deprecated because it was incorrectly returning the input key at time. To maintain the same behavior,
replace it with GetTimeAtDistanceAlongSpline. To actually get the input key, instead call GetInputKeyValueAtDistanceAlongSpline.
deprecated: Please use GetInputKeyValueAtDistanceAlongSpline to get input key at distance or GetTimeAtDistanceAlongSpline to get time value (normalized to duration) at distance (same logic as deprecated function).

Parameters:

**distance** ( _float_)

Return type:

float


---

**get_input_key_value_at_distance_along_spline**( _distance_) → `float`

Given a distance along the length of this spline, return the corresponding input key at that point
with a fractional component between the current input key and the next as a percentage.

Parameters:

**distance** ( _float_)

Return type:

float


---

**get_input_key_value_at_spline_point**( _point_index_) → `float`

Get the input key (e.g. the time) of the control point of the spline at the specified index.

Parameters:

**point\_index** ( _int32_)

Return type:

float


---

**get_input_key_value_at_time**( _time_) → `float`

Convert a time value (in the range [0, Duration]) to an input key.

Parameters:

**time** ( _float_)

Return type:

float


---

**get_leave_tangent_at_spline_point**( _point_index_, _coordinate_space_) → `Vector`

Get the leave tangent at spline point

Parameters:

- **point\_index** ( _int32_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

Vector

get\_local\_location\_and\_tangent\_at\_spline\_point( _point\_index)->(local\_location=Vector_, _local\_tangent=Vector_)

Get local location and tangent at a spline point
deprecated: Please use GetLocationAndTangentAtSplinePoint, specifying SplineCoordinateSpace::Local

Parameters:

**point\_index** ( _int32_)

Returns:

local\_location (Vector):

local\_tangent (Vector):

Return type:

tuple

get\_location\_and\_tangent\_at\_spline\_point( _point\_index_, _coordinate\_space)->(location=Vector_, _tangent=Vector_)

Get location and tangent at a spline point

Parameters:

- **point\_index** ( _int32_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Returns:

location (Vector):

tangent (Vector):

Return type:

tuple


---

**get_location_at_distance_along_spline**( _distance_, _coordinate_space_) → `Vector`

Given a distance along the length of this spline, return the point in space where this puts you

Parameters:

- **distance** ( _float_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

Vector


---

**get_location_at_spline_input_key**( _key_, _coordinate_space_) → `Vector`

Get location along spline at the provided input key value

Parameters:

- **key** ( _float_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

Vector


---

**get_location_at_spline_point**( _point_index_, _coordinate_space_) → `Vector`

Get the location at spline point

Parameters:

- **point\_index** ( _int32_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

Vector


---

**get_location_at_time**( _time_, _coordinate_space_, _use_constant_velocity=False_) → `Vector`

Given a time from 0 to the spline duration, return the point in space where this puts you

Parameters:

- **time** ( _float_)

- **coordinate\_space** ( _SplineCoordinateSpace_)

- **use\_constant\_velocity** ( _bool_)


Return type:

Vector


---

**get_num_spline_points**() → `int`

deprecated: ‘get\_num\_spline\_points’ was renamed to ‘get\_number\_of\_spline\_points’.


---

**get_number_of_property_values**( _property_name_) → `int32`

Get the number of attribute values in a specified attribute channel.

Parameters:

**property\_name** ( _Name_) – The name of the attribute channel.

Returns:

The number of attribute values in the specified channel.

Return type:

int32


---

**get_number_of_spline_points**() → `int32`

Get the number of points that make up this spline

Return type:

int32


---

**get_number_of_spline_segments**() → `int32`

Get the number of segments that make up this spline

Return type:

int32


---

**get_right_vector_at_distance_along_spline**( _distance_, _coordinate_space_) → `Vector`

Given a distance along the length of this spline, return a unit direction vector corresponding to the spline’s right vector there.

Parameters:

- **distance** ( _float_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

Vector


---

**get_right_vector_at_spline_input_key**( _key_, _coordinate_space_) → `Vector`

Get right vector at the provided input key value

Parameters:

- **key** ( _float_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

Vector


---

**get_right_vector_at_spline_point**( _point_index_, _coordinate_space_) → `Vector`

Get the right vector at spline point

Parameters:

- **point\_index** ( _int32_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

Vector


---

**get_right_vector_at_time**( _time_, _coordinate_space_, _use_constant_velocity=False_) → `Vector`

Given a time from 0 to the spline duration, return the spline’s right vector there.

Parameters:

- **time** ( _float_)

- **coordinate\_space** ( _SplineCoordinateSpace_)

- **use\_constant\_velocity** ( _bool_)


Return type:

Vector


---

**get_roll_at_distance_along_spline**( _distance_, _coordinate_space_) → `float`

Given a distance along the length of this spline, return the spline’s roll there, in degrees.

Parameters:

- **distance** ( _float_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

float


---

**get_roll_at_spline_input_key**( _key_, _coordinate_space_) → `float`

Get roll in degrees at the provided input key value

Parameters:

- **key** ( _float_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

float


---

**get_roll_at_spline_point**( _point_index_, _coordinate_space_) → `float`

Get the amount of roll at spline point, in degrees

Parameters:

- **point\_index** ( _int32_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

float


---

**get_roll_at_time**( _time_, _coordinate_space_, _use_constant_velocity=False_) → `float`

Given a time from 0 to the spline duration, return the spline’s roll there, in degrees.

Parameters:

- **time** ( _float_)

- **coordinate\_space** ( _SplineCoordinateSpace_)

- **use\_constant\_velocity** ( _bool_)


Return type:

float


---

**get_rotation_at_distance_along_spline**( _distance_, _coordinate_space_) → `Rotator`

Given a distance along the length of this spline, return a rotation corresponding to the spline’s rotation there.

Parameters:

- **distance** ( _float_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

Rotator


---

**get_rotation_at_spline_input_key**( _key_, _coordinate_space_) → `Rotator`

Get rotator corresponding to rotation along spline at the provided input key value

Parameters:

- **key** ( _float_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

Rotator


---

**get_rotation_at_spline_point**( _point_index_, _coordinate_space_) → `Rotator`

Get the rotation at spline point as a rotator

Parameters:

- **point\_index** ( _int32_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

Rotator


---

**get_rotation_at_time**( _time_, _coordinate_space_, _use_constant_velocity=False_) → `Rotator`

Given a time from 0 to the spline duration, return a rotation corresponding to the spline’s position and direction there.

Parameters:

- **time** ( _float_)

- **coordinate\_space** ( _SplineCoordinateSpace_)

- **use\_constant\_velocity** ( _bool_)


Return type:

Rotator


---

**get_scale_at_distance_along_spline**( _distance_) → `Vector`

Given a distance along the length of this spline, return the spline’s scale there.

Parameters:

**distance** ( _float_)

Return type:

Vector


---

**get_scale_at_spline_input_key**( _key_) → `Vector`

Get scale at the provided input key value

Parameters:

**key** ( _float_)

Return type:

Vector


---

**get_scale_at_spline_point**( _point_index_) → `Vector`

Get the scale at spline point

Parameters:

**point\_index** ( _int32_)

Return type:

Vector


---

**get_scale_at_time**( _time_, _use_constant_velocity=False_) → `Vector`

Given a time from 0 to the spline duration, return the spline’s scale there.

Parameters:

- **time** ( _float_)

- **use\_constant\_velocity** ( _bool_)


Return type:

Vector


---

**get_spline_length**() → `float`

Returns total length along this spline

Return type:

float


---

**get_spline_point_at**( _point_index_, _coordinate_space_) → `SplinePoint`

Gets the spline point of the spline at the specified index

Parameters:

- **point\_index** ( _int32_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

SplinePoint


---

**get_spline_point_type**( _point_index_) → `SplinePointType`

Get the type of a spline point

Parameters:

**point\_index** ( _int32_)

Return type:

SplinePointType


---

**get_tangent_at_distance_along_spline**( _distance_, _coordinate_space_) → `Vector`

Given a distance along the length of this spline, return the tangent vector of the spline there.

Parameters:

- **distance** ( _float_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

Vector


---

**get_tangent_at_spline_input_key**( _key_, _coordinate_space_) → `Vector`

Get tangent along spline at the provided input key value

Parameters:

- **key** ( _float_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

Vector


---

**get_tangent_at_spline_point**( _point_index_, _coordinate_space_) → `Vector`

Get the tangent at spline point. This fetches the Leave tangent of the point.

Parameters:

- **point\_index** ( _int32_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

Vector


---

**get_tangent_at_time**( _time_, _coordinate_space_, _use_constant_velocity=False_) → `Vector`

Given a time from 0 to the spline duration, return the spline’s tangent there.

Parameters:

- **time** ( _float_)

- **coordinate\_space** ( _SplineCoordinateSpace_)

- **use\_constant\_velocity** ( _bool_)


Return type:

Vector


---

**get_time_at_distance_along_spline**( _distance_) → `float`

Given a distance along the length of this spline, return the corresponding time at that point

Parameters:

**distance** ( _float_)

Return type:

float


---

**get_transform_at_distance_along_spline**( _distance_, _coordinate_space_, _use_scale=False_) → `Transform`

Given a distance along the length of this spline, return an FTransform corresponding to that point on the spline.

Parameters:

- **distance** ( _float_)

- **coordinate\_space** ( _SplineCoordinateSpace_)

- **use\_scale** ( _bool_)


Return type:

Transform


---

**get_transform_at_spline_input_key**( _key_, _coordinate_space_, _use_scale=False_) → `Transform`

Get transform at the provided input key value

Parameters:

- **key** ( _float_)

- **coordinate\_space** ( _SplineCoordinateSpace_)

- **use\_scale** ( _bool_)


Return type:

Transform


---

**get_transform_at_spline_point**( _point_index_, _coordinate_space_, _use_scale=False_) → `Transform`

Get the transform at spline point

Parameters:

- **point\_index** ( _int32_)

- **coordinate\_space** ( _SplineCoordinateSpace_)

- **use\_scale** ( _bool_)


Return type:

Transform


---

**get_transform_at_time**( _time_, _coordinate_space_, _use_constant_velocity=False_, _use_scale=False_) → `Transform`

Given a time from 0 to the spline duration, return the spline’s transform at the corresponding position.

Parameters:

- **time** ( _float_)

- **coordinate\_space** ( _SplineCoordinateSpace_)

- **use\_constant\_velocity** ( _bool_)

- **use\_scale** ( _bool_)


Return type:

Transform


---

**get_up_vector_at_distance_along_spline**( _distance_, _coordinate_space_) → `Vector`

Given a distance along the length of this spline, return a unit direction vector corresponding to the spline’s up vector there.

Parameters:

- **distance** ( _float_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

Vector


---

**get_up_vector_at_spline_input_key**( _key_, _coordinate_space_) → `Vector`

Get up vector at the provided input key value

Parameters:

- **key** ( _float_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

Vector


---

**get_up_vector_at_spline_point**( _point_index_, _coordinate_space_) → `Vector`

Get the up vector at spline point

Parameters:

- **point\_index** ( _int32_)

- **coordinate\_space** ( _SplineCoordinateSpace_)


Return type:

Vector


---

**get_up_vector_at_time**( _time_, _coordinate_space_, _use_constant_velocity=False_) → `Vector`

Given a time from 0 to the spline duration, return the spline’s up vector there.

Parameters:

- **time** ( _float_)

- **coordinate\_space** ( _SplineCoordinateSpace_)

- **use\_constant\_velocity** ( _bool_)


Return type:

Vector


---

**get_vector_property_at_spline_point**( _index_, _property_name_) → `Vector`

Get a metadata property vector value along the spline at spline point

Parameters:

- **index** ( _int32_)

- **property\_name** ( _Name_)


Return type:

Vector


---

**get_world_direction_at_distance_along_spline**( _distance_) → `Vector`

Given a distance along the length of this spline, return a unit direction vector of the spline tangent there, in world space.
deprecated: Please use GetDirectionAtDistanceAlongSpline, specifying SplineCoordinateSpace::World

Parameters:

**distance** ( _float_)

Return type:

Vector


---

**get_world_direction_at_time**( _time_, _use_constant_velocity=False_) → `Vector`

Given a time from 0 to the spline duration, return a unit direction vector of the spline tangent there.
deprecated: Please use GetDirectionAtTime, specifying SplineCoordinateSpace::World

Parameters:

- **time** ( _float_)

- **use\_constant\_velocity** ( _bool_)


Return type:

Vector


---

**get_world_location_at_distance_along_spline**( _distance_) → `Vector`

Given a distance along the length of this spline, return the point in world space where this puts you
deprecated: Please use GetLocationAtDistanceAlongSpline, specifying SplineCoordinateSpace::World

Parameters:

**distance** ( _float_)

Return type:

Vector


---

**get_world_location_at_spline_point**( _point_index_) → `Vector`

Get the world location at spline point
deprecated: Please use GetLocationAtSplinePoint, specifying SplineCoordinateSpace::World

Parameters:

**point\_index** ( _int32_)

Return type:

Vector


---

**get_world_location_at_time**( _time_, _use_constant_velocity=False_) → `Vector`

Given a time from 0 to the spline duration, return the point in space where this puts you
deprecated: Please use GetLocationAtTime, specifying SplineCoordinateSpace::World

Parameters:

- **time** ( _float_)

- **use\_constant\_velocity** ( _bool_)


Return type:

Vector


---

**get_world_rotation_at_distance_along_spline**( _distance_) → `Rotator`

Given a distance along the length of this spline, return a rotation corresponding to the spline’s rotation there, in world space.
deprecated: Please use GetRotationAtDistanceAlongSpline, specifying SplineCoordinateSpace::World

Parameters:

**distance** ( _float_)

Return type:

Rotator


---

**get_world_rotation_at_time**( _time_, _use_constant_velocity=False_) → `Rotator`

Given a time from 0 to the spline duration, return a rotation corresponding to the spline’s position and direction there, in world space.
deprecated: Please use GetRotationAtTime, specifying SplineCoordinateSpace::World

Parameters:

- **time** ( _float_)

- **use\_constant\_velocity** ( _bool_)


Return type:

Rotator


---

**get_world_tangent_at_distance_along_spline**( _distance_) → `Vector`

Given a distance along the length of this spline, return the tangent vector of the spline there, in world space.
deprecated: Please use GetTangentAtDistanceAlongSpline, specifying SplineCoordinateSpace::World

Parameters:

**distance** ( _float_)

Return type:

Vector


---

_property_ `input_spline_points_to_construction_script`: bool

[Read-Write] Whether the spline points should be passed to the User Construction Script so they can be further manipulated by it.
If false, they will not be visible to it, and it will not be able to influence the per-instance positions set in the editor.

**Type:**

( bool)


---

**is_closed_loop**() → `bool`

Check whether the spline is a closed loop or not

Return type:

bool


---

**remove_property_at_index**( _index_, _property_name_) → `None`

Remove an attribute value by index.

Parameters:

- **index** ( _int32_) – The index of the specified attribute.

- **property\_name** ( _Name_) – The name of the attribute channel containing the specified attribute.



---

**remove_property_channel**( _property_name_) → `bool`

Remove an attribute channel.

Parameters:

**property\_name** ( _Name_) – The name of the channel to remove.

Return type:

bool


---

**remove_spline_point**( _index_, _update_spline=True_) → `None`

Removes point at specified index from the spline

Parameters:

- **index** ( _int32_)

- **update\_spline** ( _bool_)



---

**set_closed_loop**( _closed_loop_, _update_spline=True_) → `None`

Specify whether the spline is a closed loop or not. The loop position will be at 1.0 after the last point’s input key

Parameters:

- **closed\_loop** ( _bool_)

- **update\_spline** ( _bool_)



---

**set_closed_loop_at_position**( _closed_loop_, _key_, _update_spline=True_) → `None`

Specify whether the spline is a closed loop or not, and if so, the input key corresponding to the loop point

Parameters:

- **closed\_loop** ( _bool_)

- **key** ( _float_)

- **update\_spline** ( _bool_)



---

**set_default_up_vector**( _up_vector_, _coordinate_space_) → `None`

Sets the default up vector used by this spline

Parameters:

- **up\_vector** ( _Vector_)

- **coordinate\_space** ( _SplineCoordinateSpace_)



---

**set_draw_debug**( _show_) → `None`

Specify whether this spline should be rendered when the Editor/Game spline show flag is set

Parameters:

**show** ( _bool_)


---

**set_float_property_at_index**( _index_, _value_, _property_name_) → `None`

Set a float attribute value by index.

Parameters:

- **index** ( _int32_) – The index of the specified attribute.

- **value** ( _float_) – The desired attribute value.

- **property\_name** ( _Name_) – The name of the attribute channel containing the specified attribute.



---

**set_float_property_at_spline_input_key**( _key_, _value_, _property_name_) → `int32`

Add a float attribute value by parameter.

Parameters:

- **key** ( _float_) – The desired attribute parameter.

- **value** ( _float_) – The desired attribute value.

- **property\_name** ( _Name_) – The name of the attribute channel that will contain the new attribute value.


Returns:

The index of the new attribute.

Return type:

int32


---

**set_float_property_input_key_at_index**( _index_, _key_, _property_name_) → `int32`

Set a float attribute parameter by index.

Parameters:

- **index** ( _int32_) – The index of the specified attribute.

- **key** ( _float_) – The desired attribute parameter.

- **property\_name** ( _Name_) – The name of the attribute channel containing the specified attribute.


Returns:

The index of the specified attribute after changing the attribute parameter (it can change).

Return type:

int32


---

**set_location_at_spline_point**( _point_index_, _location_, _coordinate_space_, _update_spline=True_) → `None`

Move an existing point to a new location

Parameters:

- **point\_index** ( _int32_)

- **location** ( _Vector_)

- **coordinate\_space** ( _SplineCoordinateSpace_)

- **update\_spline** ( _bool_)



---

**set_override_construction_script**( _override_) → `None`

Set the spline to be edited outside of the construction script

Parameters:

**override** ( _bool_)


---

**set_rotation_at_spline_point**( _point_index_, _rotation_, _coordinate_space_, _update_spline=True_) → `None`

Set the rotation of an existing spline point. This also aligns tangents with the forward vector of the rotation.

Parameters:

- **point\_index** ( _int32_)

- **rotation** ( _Rotator_)

- **coordinate\_space** ( _SplineCoordinateSpace_)

- **update\_spline** ( _bool_)



---

**set_scale_at_spline_point**( _point_index_, _scale_vector_, _update_spline=True_) → `None`

Set the scale at a given spline point

Parameters:

- **point\_index** ( _int32_)

- **scale\_vector** ( _Vector_)

- **update\_spline** ( _bool_)



---

**set_selected_spline_segment_color**( _segment_color_) → `None`

Specify selected spline component segment color in the editor

Parameters:

**segment\_color** ( _LinearColor_)


---

**set_spline_local_points**( _points_) → `None`

Sets the spline to an array of local space points
deprecated: Please use SetSplinePoints, specifying SplineCoordinateSpace::Local

Parameters:

**points** ( _Array_ _\_ [_Vector_ _]_)


---

**set_spline_point_type**( _point_index_, _type_, _update_spline=True_) → `None`

Specify the type of a spline point

Parameters:

- **point\_index** ( _int32_)

- **type** ( _SplinePointType_)

- **update\_spline** ( _bool_)



---

**set_spline_points**( _points_, _coordinate_space_, _update_spline=True_) → `None`

Sets the spline to an array of points

Parameters:

- **points** ( _Array_ _\_ [_Vector_ _]_)

- **coordinate\_space** ( _SplineCoordinateSpace_)

- **update\_spline** ( _bool_)



---

**set_spline_world_points**( _points_) → `None`

Sets the spline to an array of world space points
deprecated: Please use SetSplinePoints, specifying SplineCoordinateSpace::World

Parameters:

**points** ( _Array_ _\_ [_Vector_ _]_)


---

**set_tangent_at_spline_point**( _point_index_, _tangent_, _coordinate_space_, _update_spline=True_) → `None`

Specify the tangent at a given spline point

Parameters:

- **point\_index** ( _int32_)

- **tangent** ( _Vector_)

- **coordinate\_space** ( _SplineCoordinateSpace_)

- **update\_spline** ( _bool_)



---

**set_tangent_color**( _tangent_color_) → `None`

Specify selected spline component segment color in the editor

Parameters:

**tangent\_color** ( _LinearColor_)


---

**set_tangents_at_spline_point**( _point_index_, _arrive_tangent_, _leave_tangent_, _coordinate_space_, _update_spline=True_) → `None`

Specify the tangents at a given spline point

Parameters:

- **point\_index** ( _int32_)

- **arrive\_tangent** ( _Vector_)

- **leave\_tangent** ( _Vector_)

- **coordinate\_space** ( _SplineCoordinateSpace_)

- **update\_spline** ( _bool_)



---

**set_unselected_spline_segment_color**( _segment_color_) → `None`

Specify unselected spline component segment color in the editor

Parameters:

**segment\_color** ( _LinearColor_)


---

**set_up_vector_at_spline_point**( _point_index_, _up_vector_, _coordinate_space_, _update_spline=True_) → `None`

Specify the up vector at a given spline point

Parameters:

- **point\_index** ( _int32_)

- **up\_vector** ( _Vector_)

- **coordinate\_space** ( _SplineCoordinateSpace_)

- **update\_spline** ( _bool_)



---

**set_world_location_at_spline_point**( _point_index_, _location_) → `None`

Move an existing point to a new world location
deprecated: Please use SetLocationAtSplinePoint, specifying SplineCoordinateSpace::World

Parameters:

- **point\_index** ( _int32_)

- **location** ( _Vector_)



---

_property_ `stationary_endpoints`: bool

[Read-Write] Whether the endpoints of the spline are considered stationary when traversing the spline at non-constant velocity. Essentially this sets the endpoints’ tangents to zero vectors.

**Type:**

( bool)


---

**supports_attributes**() → `boolReturns:`

True if this component currently supports arbitrary attribute channels, false otherwise.

Return type:

bool


---

**update_spline**() → `None`

Update the spline tangents and SplineReparamTable

### Table of Contents

- `unreal.SplineComponent`
  - `SplineComponent`
    - `SplineComponent.add_point()`
    - `SplineComponent.add_points()`
    - `SplineComponent.add_spline_local_point()`
    - `SplineComponent.add_spline_point()`
    - `SplineComponent.add_spline_point_at_index()`
    - `SplineComponent.add_spline_world_point()`
    - `SplineComponent.b_always_render_in_editor`
    - `SplineComponent.clear_spline_points()`
    - `SplineComponent.convert_spline_segment_to_poly_line()`
    - `SplineComponent.convert_spline_to_poly_line()`
    - `SplineComponent.convert_spline_to_poly_line_with_distances()`
    - `SplineComponent.convert_spline_to_polyline_in_distance_range()`
    - `SplineComponent.convert_spline_to_polyline_in_time_range()`
    - `SplineComponent.create_float_property_channel()`
    - `SplineComponent.default_up_vector`
    - `SplineComponent.divide_spline_into_polyline_recursive()`
    - `SplineComponent.divide_spline_into_polyline_recursive_with_distances()`
    - `SplineComponent.draw_debug`
    - `SplineComponent.duration`
    - `SplineComponent.find_direction_closest_to_world_location()`
    - `SplineComponent.find_input_key_closest_to_world_location()`
    - `SplineComponent.find_input_key_on_segment_closest_to_world_location()`
    - `SplineComponent.find_location_closest_to_world_location()`
    - `SplineComponent.find_right_vector_closest_to_world_location()`
    - `SplineComponent.find_roll_closest_to_world_location()`
    - `SplineComponent.find_rotation_closest_to_world_location()`
    - `SplineComponent.find_scale_closest_to_world_location()`
    - `SplineComponent.find_tangent_closest_to_world_location()`
    - `SplineComponent.find_transform_closest_to_world_location()`
    - `SplineComponent.find_up_vector_closest_to_world_location()`
    - `SplineComponent.get_arrive_tangent_at_spline_point()`
    - `SplineComponent.get_default_up_vector()`
    - `SplineComponent.get_direction_at_distance_along_spline()`
    - `SplineComponent.get_direction_at_spline_input_key()`
    - `SplineComponent.get_direction_at_spline_point()`
    - `SplineComponent.get_direction_at_time()`
    - `SplineComponent.get_distance_along_spline_at_location()`
    - `SplineComponent.get_distance_along_spline_at_spline_input_key()`
    - `SplineComponent.get_distance_along_spline_at_spline_point()`
    - `SplineComponent.get_float_property_at_index()`
    - `SplineComponent.get_float_property_at_spline_input_key()`
    - `SplineComponent.get_float_property_at_spline_point()`
    - `SplineComponent.get_float_property_channels()`
    - `SplineComponent.get_float_property_input_key_at_index()`
    - `SplineComponent.get_input_key_at_distance_along_spline()`
    - `SplineComponent.get_input_key_value_at_distance_along_spline()`
    - `SplineComponent.get_input_key_value_at_spline_point()`
    - `SplineComponent.get_input_key_value_at_time()`
    - `SplineComponent.get_leave_tangent_at_spline_point()`
    - `SplineComponent.get_local_location_and_tangent_at_spline_point()`
    - `SplineComponent.get_location_and_tangent_at_spline_point()`
    - `SplineComponent.get_location_at_distance_along_spline()`
    - `SplineComponent.get_location_at_spline_input_key()`
    - `SplineComponent.get_location_at_spline_point()`
    - `SplineComponent.get_location_at_time()`
    - `SplineComponent.get_num_spline_points()`
    - `SplineComponent.get_number_of_property_values()`
    - `SplineComponent.get_number_of_spline_points()`
    - `SplineComponent.get_number_of_spline_segments()`
    - `SplineComponent.get_right_vector_at_distance_along_spline()`
    - `SplineComponent.get_right_vector_at_spline_input_key()`
    - `SplineComponent.get_right_vector_at_spline_point()`
    - `SplineComponent.get_right_vector_at_time()`
    - `SplineComponent.get_roll_at_distance_along_spline()`
    - `SplineComponent.get_roll_at_spline_input_key()`
    - `SplineComponent.get_roll_at_spline_point()`
    - `SplineComponent.get_roll_at_time()`
    - `SplineComponent.get_rotation_at_distance_along_spline()`
    - `SplineComponent.get_rotation_at_spline_input_key()`
    - `SplineComponent.get_rotation_at_spline_point()`
    - `SplineComponent.get_rotation_at_time()`
    - `SplineComponent.get_scale_at_distance_along_spline()`
    - `SplineComponent.get_scale_at_spline_input_key()`
    - `SplineComponent.get_scale_at_spline_point()`
    - `SplineComponent.get_scale_at_time()`
    - `SplineComponent.get_spline_length()`
    - `SplineComponent.get_spline_point_at()`
    - `SplineComponent.get_spline_point_type()`
    - `SplineComponent.get_tangent_at_distance_along_spline()`
    - `SplineComponent.get_tangent_at_spline_input_key()`
    - `SplineComponent.get_tangent_at_spline_point()`
    - `SplineComponent.get_tangent_at_time()`
    - `SplineComponent.get_time_at_distance_along_spline()`
    - `SplineComponent.get_transform_at_distance_along_spline()`
    - `SplineComponent.get_transform_at_spline_input_key()`
    - `SplineComponent.get_transform_at_spline_point()`
    - `SplineComponent.get_transform_at_time()`
    - `SplineComponent.get_up_vector_at_distance_along_spline()`
    - `SplineComponent.get_up_vector_at_spline_input_key()`
    - `SplineComponent.get_up_vector_at_spline_point()`
    - `SplineComponent.get_up_vector_at_time()`
    - `SplineComponent.get_vector_property_at_spline_point()`
    - `SplineComponent.get_world_direction_at_distance_along_spline()`
    - `SplineComponent.get_world_direction_at_time()`
    - `SplineComponent.get_world_location_at_distance_along_spline()`
    - `SplineComponent.get_world_location_at_spline_point()`
    - `SplineComponent.get_world_location_at_time()`
    - `SplineComponent.get_world_rotation_at_distance_along_spline()`
    - `SplineComponent.get_world_rotation_at_time()`
    - `SplineComponent.get_world_tangent_at_distance_along_spline()`
    - `SplineComponent.input_spline_points_to_construction_script`
    - `SplineComponent.is_closed_loop()`
    - `SplineComponent.remove_property_at_index()`
    - `SplineComponent.remove_property_channel()`
    - `SplineComponent.remove_spline_point()`
    - `SplineComponent.set_closed_loop()`
    - `SplineComponent.set_closed_loop_at_position()`
    - `SplineComponent.set_default_up_vector()`
    - `SplineComponent.set_draw_debug()`
    - `SplineComponent.set_float_property_at_index()`
    - `SplineComponent.set_float_property_at_spline_input_key()`
    - `SplineComponent.set_float_property_input_key_at_index()`
    - `SplineComponent.set_location_at_spline_point()`
    - `SplineComponent.set_override_construction_script()`
    - `SplineComponent.set_rotation_at_spline_point()`
    - `SplineComponent.set_scale_at_spline_point()`
    - `SplineComponent.set_selected_spline_segment_color()`
    - `SplineComponent.set_spline_local_points()`
    - `SplineComponent.set_spline_point_type()`
    - `SplineComponent.set_spline_points()`
    - `SplineComponent.set_spline_world_points()`
    - `SplineComponent.set_tangent_at_spline_point()`
    - `SplineComponent.set_tangent_color()`
    - `SplineComponent.set_tangents_at_spline_point()`
    - `SplineComponent.set_unselected_spline_segment_color()`
    - `SplineComponent.set_up_vector_at_spline_point()`
    - `SplineComponent.set_world_location_at_spline_point()`
    - `SplineComponent.stationary_endpoints`
    - `SplineComponent.supports_attributes()`
    - `SplineComponent.update_spline()`