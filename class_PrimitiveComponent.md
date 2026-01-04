# unreal.PrimitiveComponent

```python
class unreal.PrimitiveComponent(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``SceneComponent``


PrimitiveComponents are SceneComponents that contain or generate some sort of geometry, generally to be rendered or used as collision data.
There are several subclasses for the various types of geometry, but the most common by far are the ShapeComponents (Capsule, Sphere, Box), StaticMeshComponent, and SkeletalMeshComponent.
ShapeComponents generate geometry that is used for collision detection but are not rendered, while StaticMeshComponents and SkeletalMeshComponents contain pre-built geometry that is rendered, but can also be used for collision detection.

**C++ Source:**

- **Module**: Engine

- **File**: PrimitiveComponent.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `absolute_location` (bool): [Read-Write] If RelativeLocation should be considered relative to the world, rather than the parent

- `absolute_rotation` (bool): [Read-Write] If RelativeRotation should be considered relative to the world, rather than the parent

- `absolute_scale` (bool): [Read-Write] If RelativeScale3D should be considered relative to the world, rather than the parent

- `affect_distance_field_lighting` (bool): [Read-Write] Controls whether the primitive should affect dynamic distance field lighting methods. This flag is only used if CastShadow is true.

- `affect_dynamic_indirect_lighting` (bool): [Read-Write] Controls whether the primitive should influence indirect lighting.

- `affect_indirect_lighting_while_hidden` (bool): [Read-Write] Controls whether the primitive should affect indirect lighting when hidden. This flag is only used if bAffectDynamicIndirectLighting is true.

- `allow_cull_distance_volume` (bool): [Read-Write] Whether to accept cull distance volumes to modify cached cull distance.

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

- `component_tags` (Array[Name]): [Read-Write] Array of tags that can be used for grouping and categorizing. Can also be accessed from scripting.

- `consider_for_actor_placement_when_hidden` (bool): [Read-Write] If true, this component will be considered for placement when dragging and placing items in the editor even if it is not visible, such as in the case of hidden collision meshes

- `custom_depth_stencil_value` (int32): [Read-Write] Optionally write this 0-255 value to the stencil buffer in CustomDepth pass (Requires project setting or r.CustomDepth == 3)

- `custom_depth_stencil_write_mask` (RendererStencilMask): [Read-Write] Mask used for stencil buffer writes.

- `custom_primitive_data` (CustomPrimitiveData): [Read-Write] Optional user defined default values for the custom primitive data of this primitive

- `detail_mode` (DetailMode): [Read-Write] Set the required detail level of this component.
It will be deleted or made invisible if the world’s detail level is higher, based on platform and scalability settings.
For example, a detail mode of High may prevent this component from loading on mobile platforms.

- `editable_when_inherited` (bool): [Read-Write] True if this component can be modified when it was inherited from a parent actor class

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

- `is_editor_only` (bool): [Read-Write] If true, the component will be excluded from non-editor builds

- `ld_max_draw_distance` (float): [Read-Write] Max draw distance exposed to LDs. The real max draw distance is the min (disregarding 0) of this and volumes affecting this object.

- `light_attachments_as_group` (bool): [Read-Write] Whether to light this component and any attachments as a group. This only has effect on the root component of an attachment tree.
When enabled, attached component shadowing settings like bCastInsetShadow, bCastVolumetricTranslucentShadow, etc, will be ignored.
This is useful for improving performance when multiple movable components are attached together.

- `lighting_channels` (LightingChannels): [Read-Write] Channels that this component should be in. Lights with matching channels will affect the component.
These channels only apply to opaque materials, direct lighting, and dynamic lighting and shadowing.
Lighting channels are only supported on translucent materials using forward shading (i.e. when not using the translucency lighting volume).

- `lightmap_type` (LightmapType): [Read-Write]

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

- `replicate_physics_to_autonomous_proxy` (bool): [Read-Write] True if physics should be replicated to autonomous proxies. This should be true for

server-authoritative simulations, and false for client authoritative simulations.

- `replicate_using_registered_sub_object_list` (bool): [Read-Write] When true the replication system will only replicate the registered subobjects list
When false the replication system will instead call the virtual ReplicateSubObjects() function where the subobjects need to be manually replicated.

- `replicates` (bool): [Read-Write] Is this component currently replicating? Should the network code consider it for replication? Owning Actor must be replicating first!

- `return_material_on_move` (bool): [Read-Write] If true, component sweeps will return the material in their hit result.
see: MoveComponent(), FHitResult

- `runtime_virtual_textures` (Array[RuntimeVirtualTexture]): [Read-Write] Array of runtime virtual textures into which we draw the mesh for this actor.
The material also needs to be set up to output to a virtual texture.

- `self_shadow_only` (bool): [Read-Write] When enabled, the component will only cast a shadow on itself and not other components in the world.
This is especially useful for first person weapons, and forces bCastInsetShadow to be enabled.

- `shadow_cache_invalidation_behavior` (ShadowCacheInvalidationBehavior): [Read-Write] Control shadow invalidation behavior, in particular with respect to Virtual Shadow Maps and material effects like World Position Offset.

- `should_update_physics_volume` (bool): [Read-Write] Whether or not the cached PhysicsVolume this component overlaps should be updated when the component is moved.
see: GetPhysicsVolume()

- `single_sample_shadow_from_stationary_lights` (bool): [Read-Write] Whether the whole component should be shadowed as one from stationary lights, which makes shadow receiving much cheaper.
When enabled shadowing data comes from the volume lighting samples precomputed by Lightmass, which are very sparse.
This is currently only used on stationary directional lights.

- `static_when_not_moveable` (bool): [Read-Write] When false, the underlying physics body will contain all sim data (mass, inertia tensor, etc) even if mobility is not set to Moveable

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

**add_angular_impulse_in_degrees**( _impulse_, _bone_name='None'_, _vel_change=False_) → `None`

Add an angular impulse to a single rigid body. Good for one time instant burst.

Parameters:

- **impulse** ( _Vector_)

- **bone\_name** ( _Name_) – If a SkeletalMeshComponent, name of body to apply angular impulse to. ‘None’ indicates root body.

- **vel\_change** ( _bool_) – If true, the Strength is taken as a change in angular velocity instead of an impulse (ie. mass will have no effect).



---

**add_angular_impulse_in_radians**( _impulse_, _bone_name='None'_, _vel_change=False_) → `None`

Add an angular impulse to a single rigid body. Good for one time instant burst.

Parameters:

- **impulse** ( _Vector_)

- **bone\_name** ( _Name_) – If a SkeletalMeshComponent, name of body to apply angular impulse to. ‘None’ indicates root body.

- **vel\_change** ( _bool_) – If true, the Strength is taken as a change in angular velocity instead of an impulse (ie. mass will have no effect).



---

**add_force**( _force_, _bone_name='None'_, _accel_change=False_) → `None`

Add a force to a single rigid body.
This is like a ‘thruster’. Good for adding a burst over some (non zero) time. Should be called every frame for the duration of the force.

Parameters:

- **force** ( _Vector_) – Force vector to apply. Magnitude indicates strength of force.

- **bone\_name** ( _Name_) – If a SkeletalMeshComponent, name of body to apply force to. ‘None’ indicates root body.

- **accel\_change** ( _bool_) – If true, Force is taken as a change in acceleration instead of a physical force (i.e. mass will have no effect).



---

**add_force_at_location**( _force_, _location_, _bone_name='None'_) → `None`

Add a force to a single rigid body at a particular location in world space.
This is like a ‘thruster’. Good for adding a burst over some (non zero) time. Should be called every frame for the duration of the force.

Parameters:

- **force** ( _Vector_) – Force vector to apply. Magnitude indicates strength of force.

- **location** ( _Vector_) – Location to apply force, in world space.

- **bone\_name** ( _Name_) – If a SkeletalMeshComponent, name of body to apply force to. ‘None’ indicates root body.



---

**add_force_at_location_local**( _force_, _location_, _bone_name='None'_) → `None`

Add a force to a single rigid body at a particular location. Both Force and Location should be in body space.
This is like a ‘thruster’. Good for adding a burst over some (non zero) time. Should be called every frame for the duration of the force.

Parameters:

- **force** ( _Vector_) – Force vector to apply. Magnitude indicates strength of force.

- **location** ( _Vector_) – Location to apply force, in component space.

- **bone\_name** ( _Name_) – If a SkeletalMeshComponent, name of body to apply force to. ‘None’ indicates root body.



---

**add_force_at_position**( _force:Vector_, _location:Vector_, _bone_name:Name='None'_) → `None`

deprecated: ‘add\_force\_at\_position’ was renamed to ‘add\_force\_at\_location’.


---

**add_impulse**( _impulse_, _bone_name='None'_, _vel_change=False_) → `None`

Add an impulse to a single rigid body. Good for one time instant burst.

Parameters:

- **impulse** ( _Vector_) – Magnitude and direction of impulse to apply.

- **bone\_name** ( _Name_) – If a SkeletalMeshComponent, name of body to apply impulse to. ‘None’ indicates root body.

- **vel\_change** ( _bool_) – If true, the Strength is taken as a change in velocity instead of an impulse (ie. mass will have no effect).



---

**add_impulse_at_location**( _impulse_, _location_, _bone_name='None'_) → `None`

Add an impulse to a single rigid body at a specific location.

Parameters:

- **impulse** ( _Vector_) – Magnitude and direction of impulse to apply.

- **location** ( _Vector_) – Point in world space to apply impulse at.

- **bone\_name** ( _Name_) – If a SkeletalMeshComponent, name of bone to apply impulse to. ‘None’ indicates root body.



---

**add_impulse_at_position**( _impulse:Vector_, _location:Vector_, _bone_name:Name='None'_) → `None`

deprecated: ‘add\_impulse\_at\_position’ was renamed to ‘add\_impulse\_at\_location’.


---

**add_radial_force**( _origin_, _radius_, _strength_, _falloff_, _accel_change=False_) → `None`

Add a force to all bodies in this component, originating from the supplied world-space location.

Parameters:

- **origin** ( _Vector_) – Origin of force in world space.

- **radius** ( _float_) – Radius within which to apply the force.

- **strength** ( _float_) – Strength of force to apply.

- **falloff** ( _RadialImpulseFalloff_) – Allows you to control the strength of the force as a function of distance from Origin.

- **accel\_change** ( _bool_) – If true, Strength is taken as a change in acceleration instead of a physical force (i.e. mass will have no effect).



---

**add_radial_impulse**( _origin_, _radius_, _strength_, _falloff_, _vel_change=False_) → `None`

Add an impulse to all rigid bodies in this component, radiating out from the specified position.

Parameters:

- **origin** ( _Vector_) – Point of origin for the radial impulse blast, in world space

- **radius** ( _float_) – Size of radial impulse. Beyond this distance from Origin, there will be no affect.

- **strength** ( _float_) – Maximum strength of impulse applied to body.

- **falloff** ( _RadialImpulseFalloff_) – Allows you to control the strength of the impulse as a function of distance from Origin.

- **vel\_change** ( _bool_) – If true, the Strength is taken as a change in velocity instead of an impulse (ie. mass will have no effect).



---

**add_torque_in_degrees**( _torque_, _bone_name='None'_, _accel_change=False_) → `None`

Add a torque to a single rigid body.

Parameters:

- **torque** ( _Vector_) – Torque to apply. Direction is axis of rotation and magnitude is strength of torque.

- **bone\_name** ( _Name_) – If a SkeletalMeshComponent, name of body to apply torque to. ‘None’ indicates root body.

- **accel\_change** ( _bool_) – If true, Torque is taken as a change in angular acceleration instead of a physical torque (i.e. mass will have no effect).



---

**add_torque_in_radians**( _torque_, _bone_name='None'_, _accel_change=False_) → `None`

Add a torque to a single rigid body.

Parameters:

- **torque** ( _Vector_) – Torque to apply. Direction is axis of rotation and magnitude is strength of torque.

- **bone\_name** ( _Name_) – If a SkeletalMeshComponent, name of body to apply torque to. ‘None’ indicates root body.

- **accel\_change** ( _bool_) – If true, Torque is taken as a change in angular acceleration instead of a physical torque (i.e. mass will have no effect).



---

**add_velocity_change_impulse_at_location**( _impulse_, _location_, _bone_name='None'_) → `None`

Add an impulse to a single rigid body at a specific location. The Strength is taken as a change in angular velocity instead of an impulse (ie. mass will have no effect).

Parameters:

- **impulse** ( _Vector_) – Magnitude and direction of impulse to apply.

- **location** ( _Vector_) – Point in world space to apply impulse at.

- **bone\_name** ( _Name_) – If a SkeletalMeshComponent, name of bone to apply impulse to. ‘None’ indicates root body.



---

_property_ `affect_distance_field_lighting`: bool

[Read-Only] Controls whether the primitive should affect dynamic distance field lighting methods. This flag is only used if CastShadow is true.

**Type:**

( bool)


---

_property_ `affect_dynamic_indirect_lighting`: bool

[Read-Only] Controls whether the primitive should influence indirect lighting.

**Type:**

( bool)


---

_property_ `affect_indirect_lighting_while_hidden`: bool

[Read-Only] Controls whether the primitive should affect indirect lighting when hidden. This flag is only used if bAffectDynamicIndirectLighting is true.

**Type:**

( bool)


---

_property_ `allow_cull_distance_volume`: bool

[Read-Only] Whether to accept cull distance volumes to modify cached cull distance.

**Type:**

( bool)


---

_property_ `always_create_physics_state`: bool

[Read-Only] Indicates if we’d like to create physics state all the time (for collision and simulation).
If you set this to false, it still will create physics state if collision or simulation activated.
This can help performance if you’d like to avoid overhead of creating physics state when triggers

**Type:**

( bool)


---

_property_ `apply_impulse_on_damage`: bool

[Read-Write] True for damage to this component to apply physics impulse, false to opt out of these impulses.

**Type:**

( bool)


---

_property_ `body_instance`: BodyInstance

[Read-Only] Physics scene information for this component, holds a single rigid body with multiple shapes.

**Type:**

( BodyInstance)


---

**box_overlap_component**( _box_centre_, _box_, _trace_complex=True_, _show_trace_, _persistent_show_trace=False_) → `(hit_location=Vector,hit_normal=Vector,bone_name=Name,out_hit=HitResult)orNone`

Perform a box overlap against a single component as an AABB (No rotation)

Parameters:

- **box\_centre** ( _Vector_) – The centre of the box to overlap with the component

- **box** ( _Box_) – Description of the box to use in the overlap

- **trace\_complex** ( _bool_) – Whether or not to trace the complex physics representation or just the simple representation

- **show\_trace** ( _bool_) – Whether or not to draw the trace in the world (for debugging)

- **persistent\_show\_trace** ( _bool_) – Whether or not to make the debugging draw stay in the world permanently


Returns:

hit\_location (Vector):

hit\_normal (Vector):

bone\_name (Name):

out\_hit (HitResult):

Return type:

tuple or None


---

_property_ `cached_max_draw_distance`: float

[Read-Only] The distance to cull this primitive at.
A CachedMaxDrawDistance of 0 indicates that the primitive should not be culled by distance.

**Type:**

( float)


---

_property_ `can_be_character_base`: CanBeCharacterBase

‘can\_be\_character\_base’ was renamed to ‘can\_character\_step\_up\_on’.

**Type:**

deprecated


---

**can_character_step_up**( _pawn_) → `bool`

Return true if the given Pawn can step up onto this component.
This controls whether they can try to step up on it when they bump in to it, not whether they can walk on it after landing on it.
see: CanCharacterStepUpOn

Parameters:

**pawn** ( _Pawn_) – the Pawn that wants to step onto this component.

Return type:

bool


---

_property_ `can_character_step_up_on`: CanBeCharacterBase

[Read-Write] Determine whether a Character can step up onto this component.
This controls whether they can try to step up on it when they bump in to it, not whether they can walk on it after landing on it.
see: FWalkableSlopeOverride

**Type:**

( CanBeCharacterBase)


---

_property_ `cast_cinematic_shadow`: bool

[Read-Only] Whether this component should cast shadows from lights that have bCastShadowsFromCinematicObjectsOnly enabled.
This is useful for characters in a cinematic with special cinematic lights, where the cost of shadowmap rendering of the environment is undesired.

**Type:**

( bool)


---

_property_ `cast_contact_shadow`: bool

[Read-Only] Whether the object should cast contact shadows.
This flag is only used if CastShadow is true.

**Type:**

( bool)


---

_property_ `cast_dynamic_shadow`: bool

[Read-Only] Controls whether the primitive should cast shadows in the case of non precomputed shadowing. This flag is only used if CastShadow is true and if FirstPersonPrimitiveType is not set to FirstPerson.

**Type:**

( bool)


---

_property_ `cast_far_shadow`: bool

[Read-Only] When enabled, the component will be rendering into the far shadow cascades (only for directional lights). This flag is only used if CastShadow is true and if FirstPersonPrimitiveType is not set to FirstPerson.

**Type:**

( bool)


---

_property_ `cast_hidden_shadow`: bool

[Read-Only] If true, the primitive will cast shadows even if bHidden is true.
Controls whether the primitive should cast shadows when hidden.
This flag is only used if CastShadow is true and if FirstPersonPrimitiveType is not set to WorldSpaceRepresentation.

**Type:**

( bool)


---

_property_ `cast_inset_shadow`: bool

[Read-Only] Whether this component should create a per-object shadow that gives higher effective shadow resolution.
Useful for cinematic character shadowing. Assumed to be enabled if bSelfShadowOnly is enabled.

**Type:**

( bool)


---

_property_ `cast_shadow`: bool

[Read-Only] Controls whether the primitive component should cast a shadow or not.

**Type:**

( bool)


---

_property_ `cast_shadow_as_two_sided`: bool

[Read-Only] Whether this primitive should cast dynamic shadows as if it were a two sided material.

**Type:**

( bool)


---

_property_ `cast_static_shadow`: bool

[Read-Only] Whether the object should cast a static shadow from shadow casting lights. This flag is only used if CastShadow is true and if FirstPersonPrimitiveType is not set to FirstPerson.

**Type:**

( bool)


---

_property_ `cast_volumetric_translucent_shadow`: bool

[Read-Only] Whether the object should cast a volumetric translucent shadow.
Volumetric translucent shadows are useful for primitives with smoothly changing opacity like particles representing a volume,
but have artifacts when used on highly opaque surfaces. This flag is only used if CastShadow is true and if FirstPersonPrimitiveType is not set to FirstPerson.

**Type:**

( bool)


---

**clear_move_ignore_actors**() → `None`

Clear the list of actors we ignore when moving.


---

**clear_move_ignore_components**() → `None`

Clear the list of components we ignore when moving.


---

**copy_array_of_move_ignore_actors**() → `Array\ [Actor]`

Returns the list of actors we currently ignore when moving.

Return type:

Array\ [Actor]


---

**copy_array_of_move_ignore_components**() → `Array\ [PrimitiveComponent]`

Returns the list of actors we currently ignore when moving.

Return type:

Array\ [PrimitiveComponent]


---

**create_and_set_material_instance_dynamic**( _element_index_) → `MaterialInstanceDynamic`

Creates a Dynamic Material Instance for the specified element index. The parent of the instance is set to the material being replaced.
deprecated: Use CreateDynamicMaterialInstance instead.

Parameters:

**element\_index** ( _int32_) – The index of the skin to replace the material for. If invalid, the material is unchanged and NULL is returned.

Return type:

MaterialInstanceDynamic


---

**create_and_set_material_instance_dynamic_from_material**( _element_index_, _parent_) → `MaterialInstanceDynamic`

Creates a Dynamic Material Instance for the specified element index. The parent of the instance is set to the material being replaced.
deprecated: Use CreateDynamicMaterialInstance instead.

Parameters:

- **element\_index** ( _int32_) – The index of the skin to replace the material for. If invalid, the material is unchanged and NULL is returned.

- **parent** ( _MaterialInterface_)


Return type:

MaterialInstanceDynamic


---

**create_dynamic_material_instance**( _element_index_, _source_material=None_, _optional_name='None'_) → `MaterialInstanceDynamic`

Creates a Dynamic Material Instance for the specified element index, optionally from the supplied material.

Parameters:

- **element\_index** ( _int32_) – The index of the skin to replace the material for. If invalid, the material is unchanged and NULL is returned.

- **source\_material** ( _MaterialInterface_)

- **optional\_name** ( _Name_)


Return type:

MaterialInstanceDynamic


---

_property_ `custom_depth_stencil_value`: int

[Read-Only] Optionally write this 0-255 value to the stencil buffer in CustomDepth pass (Requires project setting or r.CustomDepth == 3)

**Type:**

(int32)


---

_property_ `custom_depth_stencil_write_mask`: RendererStencilMask

[Read-Only] Mask used for stencil buffer writes.

**Type:**

( RendererStencilMask)


---

_property_ `emissive_light_source`: bool

[Read-Only] Whether the primitive will be used as an emissive light source.

**Type:**

( bool)


---

_property_ `enable_auto_lod_generation`: bool

[Read-Write] Whether to include this component in HLODs or not.

**Type:**

( bool)


---

_property_ `exclude_for_specific_hlod_levels`: None

[Read-Write]
deprecated: WARNING: This property has been deprecated, use the SetExcludedFromHLODLevel/IsExcludedFromHLODLevel functions instead

**Type:**

( Array[int32])


---

_property_ `exclude_from_light_attachment_group`: bool

[Read-Only] If set, then it overrides any bLightAttachmentsAsGroup set in a parent.

**Type:**

( bool)


---

_property_ `first_person_primitive_type`: FirstPersonPrimitiveType

[Read-Only] If this is set to FirstPerson, the camera FirstPersonFieldOfView and FirstPersonScale parameters will be used on this component. These parameters can be used to render the component with a different field of view and a smaller depth range such that clipping with the scene can be avoided. This is useful for rendering first person view geometry.

**Type:**

( FirstPersonPrimitiveType)


---

_property_ `force_mip_streaming`: bool

[Read-Only] If true, forces mips for textures used by this component to be resident when this component’s level is loaded.

**Type:**

( bool)


---

_property_ `generate_overlap_events`: bool

[Read-Write]

**Type:**

( bool)


---

**get_angular_damping**() → `float`

Returns the angular damping of this component.

Return type:

float


---

**get_body_instance_async_physics_tick_handle**( _bone_name='None'_, _get_welded=True_, _index=-1_) → `BodyInstanceAsyncPhysicsTickHandle`

Returns BodyInstanceAsyncPhysicsTickHandle of the component. For use in the Async Physics Tick event

Parameters:

- **bone\_name** ( _Name_) – Used to get body associated with specific bone. NAME\_None automatically gets the root most body

- **get\_welded** ( _bool_) – If the component has been welded to another component and bGetWelded is true we return the single welded BodyInstance that is used in the simulation

- **index** ( _int32_) – Index used in Components with multiple body instances


Returns:

Returns the BodyInstanceAsyncPhysicsTickHandle based on various states (does component have multiple bodies? Is the body welded to another body?)

Return type:

BodyInstanceAsyncPhysicsTickHandle


---

**get_center_of_mass**( _bone_name='None'_) → `Vector`

Get the center of mass of a single body. In the case of a welded body this will return the center of mass of the entire welded body (including its parent and children)
Objects that are not simulated return (0,0,0) as they do not have COM

Parameters:

**bone\_name** ( _Name_) – If a SkeletalMeshComponent, name of body to get center of mass of. ‘None’ indicates root body.

Return type:

Vector

get\_closest\_point\_on\_collision( _point_, _bone\_name="None")->(float_, _out\_point\_on\_body=Vector_)

Returns the distance and closest point to the collision surface.
Component must have simple collision to be queried for closest point.

Parameters:

- **point** ( _Vector_) – World 3D vector

- **bone\_name** ( _Name_) – If a SkeletalMeshComponent, name of body to set center of mass of. ‘None’ indicates root body.


Returns:

Success if returns > 0.f, if returns 0.f, it is either not convex or inside of the point If returns < 0.f, this primitive does not have collsion

out\_point\_on\_body (Vector): Point on the surface of collision closest to Point

Return type:

Vector


---

**get_collision_enabled**() → `CollisionEnabled`

Returns the form of collision for this component

Return type:

CollisionEnabled


---

**get_collision_object_type**() → `CollisionChannel`

Gets the collision object type

Return type:

CollisionChannel


---

**get_collision_profile_name**() → `Name`

Get the collision profile name

Return type:

Name


---

**get_collision_response_to_channel**( _channel_) → `CollisionResponseType`

Gets the response type given a specific channel

Parameters:

**channel** ( _CollisionChannel_)

Return type:

CollisionResponseType


---

**get_custom_primitive_data_index_for_scalar_parameter**( _parameter_name_) → `int32`

Gets the index of the scalar parameter for the custom primitive data array

Parameters:

**parameter\_name** ( _Name_) – The parameter name of the custom primitive

Returns:

The index of the custom primitive, INDEX\_NONE (-1) if not found

Return type:

int32


---

**get_custom_primitive_data_index_for_vector_parameter**( _parameter_name_) → `int32`

Gets the index of the vector parameter for the custom primitive data array

Parameters:

**parameter\_name** ( _Name_) – The parameter name of the custom primitive

Returns:

The index of the custom primitive, INDEX\_NONE (-1) if not found

Return type:

int32


---

**get_editor_material**( _element_index_) → `MaterialInterface`

Returns the material to show in the editor details panel as being used. Skips Nanite Override materials.

Parameters:

**element\_index** ( _int32_)

Return type:

MaterialInterface


---

**get_gyroscopic_torque_enabled**() → `bool`

Returns whether this component is affected by gyroscopic torque.

Return type:

bool


---

**get_ignore_bounds_for_editor_focus**() → `bool`

Whether or not the bounds of this component should be considered when focusing the editor camera to an actor with this component in it.
Useful for debug components which need a bounds for rendering but don’t contribute to the visible part of the mesh in a meaningful way

Return type:

bool


---

**get_inertia_tensor**( _bone_name='None'_) → `Vector`

Returns the inertia tensor of this component in kg cm^2. The inertia tensor is in local component space.

Parameters:

**bone\_name** ( _Name_)

Return type:

Vector


---

**get_linear_damping**() → `float`

Returns the linear damping of this component.

Return type:

float


---

**get_mass**() → `float`

Returns the mass of this component in kg.

Return type:

float


---

**get_mass_scale**( _bone_name='None'_) → `float`

Returns the mass scale used to calculate the mass of a single physics body

Parameters:

**bone\_name** ( _Name_)

Return type:

float


---

**get_material**( _element_index_) → `MaterialInterface`

Returns the material used by the element at the specified index

Parameters:

**element\_index** ( _int32_) – The element to access the material of.

Returns:

the material used by the indexed element of this mesh.

Return type:

MaterialInterface


---

**get_material_by_name**( _material_slot_name_) → `MaterialInterface`

Returns the material used by the element in the slot with the specified name.

Parameters:

**material\_slot\_name** ( _Name_) – The slot name to access the material of.

Returns:

the material used in the slot specified, or null if none exists or the slot name is not found.

Return type:

MaterialInterface

get\_material\_from\_collision\_face\_index( _face\_index)->(MaterialInterface_, _section\_index=int32_)

Try and retrieve the material applied to a particular collision face of mesh. Used with face index returned from collision trace.

Parameters:

**face\_index** ( _int32_) – Face index from hit result that was hit by a trace

Returns:

Material applied to section that the hit face belongs to

section\_index (int32): Section of the mesh that the face belongs to

Return type:

int32


---

**get_material_index**( _material_slot_name_) → `int32`

Get Material Index

Parameters:

**material\_slot\_name** ( _Name_)

Return type:

int32


---

**get_material_slot_names**() → `Array\ [Name]`

Get Material Slot Names

Return type:

Array\ [Name]


---

**get_max_depenetration_velocity**( _bone_name='None'_) → `float`

The maximum velocity used to depenetrate this object from others when spawned or teleported with initial overlaps (does not affect overlaps as a result of normal movement).
A value of zero will allow objects that are spawned overlapping to go to sleep without moving rather than pop out of each other. E.g., use zero if you spawn dynamic rocks
partially embedded in the ground and want them to be interactive but not pop out of the ground when touched.
A negative value means that the config setting CollisionInitialOverlapDepenetrationVelocity will be used.

Parameters:

**bone\_name** ( _Name_)

Return type:

float


---

**get_move_ignore_actors**() → `None`

deprecated: ‘get\_move\_ignore\_actors’ was renamed to ‘copy\_array\_of\_move\_ignore\_actors’.


---

**get_num_materials**() → `int32`

Return number of material elements in this primitive

Return type:

int32


---

**get_overlapping_actors**( _class_filter=None_) → `Array\ [Actor]`

Returns a list of actors that this component is overlapping.

Parameters:

**class\_filter** ( _type_ _(_ _Class_ _)_) – [optional] If set, only returns actors of this class or subclasses

Returns:

overlapping\_actors (Array[Actor]): [out] Returned list of overlapping actors

Return type:

Array\ [Actor]


---

**get_overlapping_components**() → `Array\ [PrimitiveComponent]`

Returns unique list of components this component is overlapping.

Returns:

out\_overlapping\_components (Array[PrimitiveComponent]):

Return type:

Array\ [PrimitiveComponent]


---

**get_physics_angular_velocity_in_degrees**( _bone_name='None'_) → `Vector`

Get the angular velocity of a single body, in degrees per second.

Parameters:

**bone\_name** ( _Name_) – If a SkeletalMeshComponent, name of body to get velocity of. ‘None’ indicates root body.

Return type:

Vector


---

**get_physics_angular_velocity_in_radians**( _bone_name='None'_) → `Vector`

Get the angular velocity of a single body, in radians per second.

Parameters:

**bone\_name** ( _Name_) – If a SkeletalMeshComponent, name of body to get velocity of. ‘None’ indicates root body.

Return type:

Vector


---

**get_physics_linear_velocity**( _bone_name='None'_) → `Vector`

Get the linear velocity of a single body.

Parameters:

**bone\_name** ( _Name_) – If a SkeletalMeshComponent, name of body to get velocity of. ‘None’ indicates root body.

Return type:

Vector


---

**get_physics_linear_velocity_at_point**( _point_, _bone_name='None'_) → `Vector`

Get the linear velocity of a point on a single body.

Parameters:

- **point** ( _Vector_) – Point is specified in world space.

- **bone\_name** ( _Name_) – If a SkeletalMeshComponent, name of body to get velocity of. ‘None’ indicates root body.


Return type:

Vector


---

**get_rb_linear_velocity**( _bone_name:Name='None'_) → `Vector`

deprecated: ‘get\_rb\_linear\_velocity’ was renamed to ‘get\_physics\_linear\_velocity’.


---

**get_static_when_not_moveable**() → `bool`

Get Static when Not Moveable

Return type:

bool


---

**get_touching_actors**( _class_filter:Class=Ellipsis_) → `None`

deprecated: ‘get\_touching\_actors’ was renamed to ‘get\_overlapping\_actors’.


---

**get_touching_components**() → `None`

deprecated: ‘get\_touching\_components’ was renamed to ‘get\_overlapping\_components’.


---

**get_update_kinematic_from_simulation**() → `bool`

Returns whether this component should be updated by simulation when it is kinematic.

Return type:

bool


---

**get_walkable_slope_override**() → `WalkableSlopeOverride`

Returns the slope override struct for this component.

Return type:

WalkableSlopeOverride


---

_property_ `has_per_instance_hit_proxies`: bool

[Read-Write] If true a hit-proxy will be generated for each instance of instanced static meshes.
This allows for other systems, like selection in viewports, to function at the individual instance.

**Type:**

( bool)


---

_property_ `hidden_in_scene_capture`: bool

[Read-Only] When true, will not be captured by Scene Capture

**Type:**

( bool)


---

_property_ `hlod_batching_policy`: HLODBatchingPolicy

[Read-Write] Determines how the geometry of a component will be incorporated in proxy (simplified) HLODs.

**Type:**

( HLODBatchingPolicy)


---

_property_ `holdout`: bool

[Read-Only] If this is True, this primitive will render black with an alpha of 0, but all secondary effects (shadows, reflections, indirect lighting) remain. This feature requires activating the project setting(s) “Alpha Output”, and “Support Primitive Alpha Holdout” if using the deferred renderer.

**Type:**

( bool)


---

**ignore_actor_when_moving**( _actor_, _should_ignore_) → `None`

Tells this component whether to ignore collision with all components of a specific Actor when this component is moved.
Components on the other Actor may also need to be told to do the same when they move.
Does not affect movement of this component when simulating physics.

Parameters:

- **actor** ( _Actor_)

- **should\_ignore** ( _bool_)



---

**ignore_component_when_moving**( _component_, _should_ignore_) → `None`

Tells this component whether to ignore collision with another component when this component is moved.
The other components may also need to be told to do the same when they move.
Does not affect movement of this component when simulating physics.

Parameters:

- **component** ( _PrimitiveComponent_)

- **should\_ignore** ( _bool_)



---

_property_ `ignore_radial_force`: bool

[Read-Write] Will ignore radial forces applied to this component.

**Type:**

( bool)


---

_property_ `ignore_radial_impulse`: bool

[Read-Write] Will ignore radial impulses applied to this component.

**Type:**

( bool)


---

_property_ `indirect_lighting_cache_quality`: IndirectLightingCacheQuality

[Read-Only] Quality of indirect lighting for Movable primitives. This has a large effect on Indirect Lighting Cache update time.

**Type:**

( IndirectLightingCacheQuality)


---

**invalidate_lumen_surface_cache**() → `None`

Invalidates Lumen surface cache and forces it to be refreshed. Useful to make material updates more responsive.


---

**is_any_rigid_body_awake**() → `bool`

Returns if any body in this component is currently awake and simulating.

Return type:

bool


---

**is_collision_enabled**() → `bool`

Utility to see if there is any form of collision (query or physics) enabled on this component.

Return type:

bool


---

**is_excluded_from_hlod_level**( _hlod_level_) → `bool`

Whether this primitive is excluded from the specified HLOD level

Parameters:

**hlod\_level** ( _HLODLevelExclusion_)

Return type:

bool


---

**is_gravity_enabled**() → `bool`

Returns whether this component is affected by gravity. Returns always false if the component is not simulated.

Return type:

bool


---

**is_material_slot_name_valid**( _material_slot_name_) → `bool`

Is Material Slot Name Valid

Parameters:

**material\_slot\_name** ( _Name_)

Return type:

bool


---

**is_overlapping_actor**( _other_) → `bool`

Check whether this component is overlapping any component of the given Actor.

Parameters:

**other** ( _Actor_) – Actor to test this component against.

Returns:

Whether this component is overlapping any component of the given Actor.

Return type:

bool


---

**is_overlapping_component**( _other_comp_) → `bool`

Check whether this component is overlapping another component.

Parameters:

**other\_comp** ( _PrimitiveComponent_) – Component to test this component against.

Returns:

Whether this component is overlapping another component.

Return type:

bool


---

**is_physics_collision_enabled**() → `bool`

Utility to see if there is any physics collision enabled on this component.

Return type:

bool


---

**is_query_collision_enabled**() → `bool`

Utility to see if there is any query collision enabled on this component.

Return type:

bool


---

_property_ `ld_max_draw_distance`: float

[Read-Only] Max draw distance exposed to LDs. The real max draw distance is the min (disregarding 0) of this and volumes affecting this object.

**Type:**

( float)


---

_property_ `light_attachments_as_group`: bool

[Read-Only] Whether to light this component and any attachments as a group. This only has effect on the root component of an attachment tree.
When enabled, attached component shadowing settings like bCastInsetShadow, bCastVolumetricTranslucentShadow, etc, will be ignored.
This is useful for improving performance when multiple movable components are attached together.

**Type:**

( bool)


---

_property_ `lighting_channels`: LightingChannels

[Read-Only] Channels that this component should be in. Lights with matching channels will affect the component.
These channels only apply to opaque materials, direct lighting, and dynamic lighting and shadowing.
Lighting channels are only supported on translucent materials using forward shading (i.e. when not using the translucency lighting volume).

**Type:**

( LightingChannels)


---

_property_ `lightmap_type`: LightmapType

[Read-Only]

**Type:**

( LightmapType)


---

**line_trace_component**( _trace_start_, _trace_end_, _trace_complex=True_, _show_trace_, _persistent_show_trace=False_) → `(hit_location=Vector,hit_normal=Vector,bone_name=Name,out_hit=HitResult)orNone`

Perform a line trace against a single component

Parameters:

- **trace\_start** ( _Vector_) – The start of the trace in world-space

- **trace\_end** ( _Vector_) – The end of the trace in world-space

- **trace\_complex** ( _bool_) – Whether or not to trace the complex physics representation or just the simple representation

- **show\_trace** ( _bool_) – Whether or not to draw the trace in the world (for debugging)

- **persistent\_show\_trace** ( _bool_) – Whether or not to make the debugging draw stay in the world permanently


Returns:

hit\_location (Vector):

hit\_normal (Vector):

bone\_name (Name):

out\_hit (HitResult):

Return type:

tuple or None


---

_property_ `min_draw_distance`: float

[Read-Only] The minimum distance at which the primitive should be rendered,
measured in world space units from the center of the primitive’s bounding sphere to the camera position.

**Type:**

( float)


---

_property_ `multi_body_overlap`: bool

[Read-Write] If true, this component will generate individual overlaps for each overlapping physics body if it is a multi-body component. When false, this component will
generate only one overlap, regardless of how many physics bodies it has and how many of them are overlapping another component/body. This flag has no
influence on single body components.

**Type:**

( bool)


---

_property_ `never_distance_cull`: bool

[Read-Only] When enabled this object will not be culled by distance. This is ignored if a child of a HLOD.

**Type:**

( bool)


---

_property_ `on_begin_cursor_over`: ComponentBeginCursorOverSignature

[Read-Write] Event called when the mouse cursor is moved over this component and mouse over events are enabled in the player controller

**Type:**

( ComponentBeginCursorOverSignature)


---

_property_ `on_clicked`: ComponentOnClickedSignature

[Read-Write] Event called when the left mouse button is clicked while the mouse is over this component and click events are enabled in the player controller

**Type:**

( ComponentOnClickedSignature)


---

_property_ `on_component_begin_overlap`: ComponentBeginOverlapSignature

[Read-Write] Event called when something starts to overlaps this component, for example a player walking into a trigger.
For events when objects have a blocking collision, for example a player hitting a wall, see ‘Hit’ events.
note: Both this component and the other one must have GetGenerateOverlapEvents() set to true to generate overlap events.
note: When receiving an overlap from another object’s movement, the directions of ‘Hit.Normal’ and ‘Hit.ImpactNormal’ will be adjusted to indicate force from the other object against this object.

**Type:**

( ComponentBeginOverlapSignature)


---

_property_ `on_component_end_overlap`: ComponentEndOverlapSignature

[Read-Write] Event called when something stops overlapping this component
note: Both this component and the other one must have GetGenerateOverlapEvents() set to true to generate overlap events.

**Type:**

( ComponentEndOverlapSignature)


---

_property_ `on_component_hit`: ComponentHitSignature

[Read-Write] Event called when a component hits (or is hit by) something solid. This could happen due to things like Character movement, using Set Location with ‘sweep’ enabled, or physics simulation.
For events when objects overlap (e.g. walking into a trigger) see the ‘Overlap’ event.
note: For collisions during physics simulation to generate hit events, ‘Simulation Generates Hit Events’ must be enabled for this component.
note: When receiving a hit from another object’s movement, the directions of ‘Hit.Normal’ and ‘Hit.ImpactNormal’ will be adjusted to indicate force from the other object against this object.
note: NormalImpulse will be filled in for physics-simulating bodies, but will be zero for swept-component blocking collisions.

**Type:**

( ComponentHitSignature)


---

_property_ `on_component_physics_state_changed`: ComponentPhysicsStateChanged

[Read-Write] Event called when physics state is created or destroyed for this component

**Type:**

( ComponentPhysicsStateChanged)


---

_property_ `on_component_sleep`: ComponentSleepSignature

[Read-Write] Event called when the underlying physics objects is put to sleep

**Type:**

( ComponentSleepSignature)


---

_property_ `on_component_wake`: ComponentWakeSignature

[Read-Write] Event called when the underlying physics objects is woken up

**Type:**

( ComponentWakeSignature)


---

_property_ `on_end_cursor_over`: ComponentEndCursorOverSignature

[Read-Write] Event called when the mouse cursor is moved off this component and mouse over events are enabled in the player controller

**Type:**

( ComponentEndCursorOverSignature)


---

_property_ `on_input_touch_begin`: ComponentOnInputTouchBeginSignature

[Read-Write] Event called when a touch input is received over this component when touch events are enabled in the player controller

**Type:**

( ComponentOnInputTouchBeginSignature)


---

_property_ `on_input_touch_end`: ComponentOnInputTouchEndSignature

[Read-Write] Event called when a touch input is released over this component when touch events are enabled in the player controller

**Type:**

( ComponentOnInputTouchEndSignature)


---

_property_ `on_input_touch_enter`: ComponentBeginTouchOverSignature

[Read-Write] Event called when a finger is moved over this component when touch over events are enabled in the player controller

**Type:**

( ComponentBeginTouchOverSignature)


---

_property_ `on_input_touch_leave`: ComponentEndTouchOverSignature

[Read-Write] Event called when a finger is moved off this component when touch over events are enabled in the player controller

**Type:**

( ComponentEndTouchOverSignature)


---

_property_ `on_released`: ComponentOnReleasedSignature

[Read-Write] Event called when the left mouse button is released while the mouse is over this component click events are enabled in the player controller

**Type:**

( ComponentOnReleasedSignature)


---

_property_ `only_owner_see`: bool

[Read-Only] If this is True, this component will only be visible when the view actor is the component’s owner, directly or indirectly.

**Type:**

( bool)


---

_property_ `owner_no_see`: bool

[Read-Only] If this is True, this component won’t be visible when the view actor is the component’s owner, directly or indirectly. Will be internally set to true when FirstPersonPrimitiveType is set to WorldSpaceRepresentation.

**Type:**

( bool)


---

**put_rigid_body_to_sleep**( _bone_name='None'_) → `None`

Force a single body back to sleep.

Parameters:

**bone\_name** ( _Name_) – If a SkeletalMeshComponent, name of body to put to sleep. ‘None’ indicates root body.


---

_property_ `ray_tracing_group_culling_priority`: RayTracingGroupCullingPriority

[Read-Only] Defines how quickly it should be culled. For example buildings should have a low priority, but small dressing should have a high priority.

**Type:**

( RayTracingGroupCullingPriority)


---

_property_ `ray_tracing_group_id`: int

[Read-Only] Defines run-time groups of components. For example allows to assemble multiple parts of a building at runtime.
-1 means that component doesn’t belong to any group.

**Type:**

(int32)


---

_property_ `receive_mobile_csm_shadows`: bool

[Read-Only] Mobile only:
If disabled this component will not receive CSM shadows. (Components that do not receive CSM may have reduced shading cost)

**Type:**

( bool)


---

_property_ `receives_decals`: bool

[Read-Only] Whether the primitive receives decals.

**Type:**

( bool)


---

**register_as_focal_point_in_physics_replication_lod**() → `None`

Register this components physics object as a focal particle in Physics Replication LOD


---

_property_ `render_custom_depth`: bool

[Read-Only] If true, this component will be rendered in the CustomDepth pass (usually used for outlines)

**Type:**

( bool)


---

_property_ `render_in_depth_pass`: bool

[Read-Only] If true, this component will be rendered in the depth pass even if it’s not rendered in the main pass

**Type:**

( bool)


---

_property_ `render_in_main_pass`: bool

[Read-Only] If true, this component will be rendered in the main pass (z prepass, basepass, transparency)

**Type:**

( bool)


---

_property_ `replicate_physics_to_autonomous_proxy`: bool

[Read-Write] True if physics should be replicated to autonomous proxies. This should be true for
server-authoritative simulations, and false for client authoritative simulations.

**Type:**

( bool)


---

_property_ `return_material_on_move`: bool

[Read-Write] If true, component sweeps will return the material in their hit result.
see: MoveComponent(), FHitResult

**Type:**

( bool)


---

_property_ `runtime_virtual_textures`: None

[Read-Write] Array of runtime virtual textures into which we draw the mesh for this actor.
The material also needs to be set up to output to a virtual texture.

**Type:**

( Array\ [RuntimeVirtualTexture])


---

**scale_by_moment_of_inertia**( _input_vector_, _bone_name='None'_) → `Vector`

Scales the given vector by the world space moment of inertia. Useful for computing the torque needed to rotate an object.

Parameters:

- **input\_vector** ( _Vector_)

- **bone\_name** ( _Name_)


Return type:

Vector


---

_property_ `self_shadow_only`: bool

[Read-Only] When enabled, the component will only cast a shadow on itself and not other components in the world.
This is especially useful for first person weapons, and forces bCastInsetShadow to be enabled.

**Type:**

( bool)


---

**set_affect_distance_field_lighting**( _new_affect_distance_field_lighting_) → `None`

Changes the value of Affect Distance Field Lighting

Parameters:

**new\_affect\_distance\_field\_lighting** ( _bool_)


---

**set_affect_dynamic_indirect_lighting**( _new_affect_dynamic_indirect_lighting_) → `None`

Changes the value of bAffectDynamicIndirectLighting

Parameters:

**new\_affect\_dynamic\_indirect\_lighting** ( _bool_)


---

**set_affect_indirect_lighting_while_hidden**( _new_affect_indirect_lighting_while_hidden_) → `None`

Changes the value of bAffectIndirectLightingWhileHidden

Parameters:

**new\_affect\_indirect\_lighting\_while\_hidden** ( _bool_)


---

**set_all_allow_partial_island_sleep**( _allow_partial_island_sleep=True_) → `None[EXPERIMENTAL] Set whether all bodies in this component allow Partial Island Sleeping for the island they are in.`

Note that Partial Island Sleeping is a CPU optimization disabling non-moving bodies in the solver.
This feature is useful for scenes with many rigid bodies but can affect the physics behavior.

Parameters:

**allow\_partial\_island\_sleep** ( _bool_)


---

**set_all_mass_scale**( _mass_scale=1.000000_) → `None`

Change the mass scale used fo all bodies in this component

Parameters:

**mass\_scale** ( _float_)


---

**set_all_physics_angular_velocity_in_degrees**( _new_ang_vel_, _add_to_current=False_) → `None`

Set the angular velocity of all bodies in this component.

Parameters:

- **new\_ang\_vel** ( _Vector_) – New angular velocity to apply to physics, in degrees per second.

- **add\_to\_current** ( _bool_) – If true, NewAngVel is added to the existing angular velocity of all bodies.



---

**set_all_physics_angular_velocity_in_radians**( _new_ang_vel_, _add_to_current=False_) → `None`

Set the angular velocity of all bodies in this component.

Parameters:

- **new\_ang\_vel** ( _Vector_) – New angular velocity to apply to physics, in radians per second.

- **add\_to\_current** ( _bool_) – If true, NewAngVel is added to the existing angular velocity of all bodies.



---

**set_all_physics_linear_velocity**( _new_vel_, _add_to_current=False_) → `None`

Set the linear velocity of all bodies in this component.

Parameters:

- **new\_vel** ( _Vector_) – New linear velocity to apply to physics.

- **add\_to\_current** ( _bool_) – If true, NewVel is added to the existing velocity of the body.



---

**set_all_rb_linear_velocity**( _new_vel:Vector_, _add_to_current:bool=False_) → `None`

deprecated: ‘set\_all\_rb\_linear\_velocity’ was renamed to ‘set\_all\_physics\_linear\_velocity’.


---

**set_all_use_ccd**( _use_ccd_) → `None`

Set whether all bodies in this component should use Continuous Collision Detection

Parameters:

**use\_ccd** ( _bool_)


---

**set_all_use_macd**( _use_macd_) → `None`

[EXPERIMENTAL] Set whether all bodies in this component should use Motion-Aware Collision Detection

Parameters:

**use\_macd** ( _bool_)


---

**set_allow_partial_island_sleep**( _allow_partial_island_sleep=True_, _bone_name='None'_) → `None[EXPERIMENTAL] Set whether this component allows Partial Island Sleeping for the island it is in.`

Note that Partial Island Sleeping is a CPU optimization disabling non-moving bodies in the solver.
This feature is useful for scenes with many rigid bodies but can affect the physics behavior.

Parameters:

- **allow\_partial\_island\_sleep** ( _bool_)

- **bone\_name** ( _Name_)



---

**set_angular_damping**( _damping_) → `None`

Sets the angular damping of this component.

Parameters:

**damping** ( _float_)


---

**set_bounds_scale**( _new_bounds_scale=1.000000_) → `None`

Scale the bounds of this object, used for frustum culling. Useful for features like WorldPositionOffset.

Parameters:

**new\_bounds\_scale** ( _float_)


---

**set_cast_contact_shadow**( _cast_contact_shadow_) → `None`

Changes the value of bCastContactShadow.

Parameters:

**cast\_contact\_shadow** ( _bool_)


---

**set_cast_hidden_shadow**( _new_cast_hidden_shadow_) → `None`

Changes the value of CastHiddenShadow.

Parameters:

**new\_cast\_hidden\_shadow** ( _bool_)


---

**set_cast_inset_shadow**( _cast_inset_shadow_) → `None`

Changes the value of CastInsetShadow.

Parameters:

**cast\_inset\_shadow** ( _bool_)


---

**set_cast_shadow**( _new_cast_shadow_) → `None`

Changes the value of CastShadow.

Parameters:

**new\_cast\_shadow** ( _bool_)


---

**set_center_of_mass**( _center_of_mass_offset_, _bone_name='None'_) → `None`

Set the center of mass of a single body. This will offset the physx-calculated center of mass.
Note that in the case where multiple bodies are attached together, the center of mass will be set for the entire group.

Parameters:

- **center\_of\_mass\_offset** ( _Vector_) – User specified offset for the center of mass of this object, from the calculated location.

- **bone\_name** ( _Name_) – If a SkeletalMeshComponent, name of body to set center of mass of. ‘None’ indicates root body.



---

**set_collision_enabled**( _new_type_) → `None`

Controls what kind of collision is enabled for this body

Parameters:

**new\_type** ( _CollisionEnabled_)


---

**set_collision_object_type**( _channel_) → `None`

Changes the collision channel that this object uses when it moves

Parameters:

**channel** ( _CollisionChannel_) – The new channel for this component to use


---

**set_collision_profile_name**( _collision_profile_name_, _update_overlaps=True_) → `None`

Set Collision Profile Name
This function is called by constructors when they set ProfileName
This will change current CollisionProfileName to be this, and overwrite Collision Setting

Parameters:

- **collision\_profile\_name** ( _Name_) – : New Profile Name

- **update\_overlaps** ( _bool_)



---

**set_collision_response_to_all_channels**( _new_response_) → `None`

Changes all ResponseToChannels container for this PrimitiveComponent. to be NewResponse

Parameters:

**new\_response** ( _CollisionResponseType_) – What the new response should be to the supplied Channel


---

**set_collision_response_to_channel**( _channel_, _new_response_) → `None`

Changes a member of the ResponseToChannels container for this PrimitiveComponent.

Parameters:

- **channel** ( _CollisionChannel_) – The channel to change the response of

- **new\_response** ( _CollisionResponseType_) – What the new response should be to the supplied Channel



---

**set_constraint_mode**( _constraint_mode_) → `None`

Sets the constraint mode of the component.

Parameters:

**constraint\_mode** ( _DOFMode_) – The type of constraint to use.


---

**set_cull_distance**( _new_cull_distance_) → `None`

Changes the value of CullDistance.

Parameters:

**new\_cull\_distance** ( _float_) – The value to assign to CullDistance.


---

**set_custom_depth_stencil_value**( _value_) → `None`

Sets the CustomDepth stencil value (0 - 255) and marks the render state dirty.

Parameters:

**value** ( _int32_)


---

**set_custom_depth_stencil_write_mask**( _write_mask_bit_) → `None`

Sets the CustomDepth stencil write mask and marks the render state dirty.

Parameters:

**write\_mask\_bit** ( _RendererStencilMask_)


---

**set_custom_primitive_data_float**( _data_index_, _value_) → `None`

Set custom primitive data at index DataIndex. This sets the run-time data only, so it doesn’t serialize.

Parameters:

- **data\_index** ( _int32_)

- **value** ( _float_)



---

**set_custom_primitive_data_float_array**( _data_index_, _values_) → `None`

Set custom primitive data, an array of floats at once, from index DataIndex to index DataIndex + Values.Num(). This sets the run-time data only, so it doesn’t serialize.

Parameters:

- **data\_index** ( _int32_)

- **values** ( _Array_ _\_ [_float_ _]_)



---

**set_custom_primitive_data_vector2**( _data_index_, _value_) → `None`

Set custom primitive data, two floats at once, from index DataIndex to index DataIndex + 1. This sets the run-time data only, so it doesn’t serialize.

Parameters:

- **data\_index** ( _int32_)

- **value** ( _Vector2D_)



---

**set_custom_primitive_data_vector3**( _data_index_, _value_) → `None`

Set custom primitive data, three floats at once, from index DataIndex to index DataIndex + 2. This sets the run-time data only, so it doesn’t serialize.

Parameters:

- **data\_index** ( _int32_)

- **value** ( _Vector_)



---

**set_custom_primitive_data_vector4**( _data_index_, _value_) → `None`

Set custom primitive data, four floats at once, from index DataIndex to index DataIndex + 3. This sets the run-time data only, so it doesn’t serialize.

Parameters:

- **data\_index** ( _int32_)

- **value** ( _Vector4_)



---

**set_default_custom_primitive_data_float**( _data_index_, _value_) → `None`

Set default custom primitive data at index DataIndex, and marks the render state dirty

Parameters:

- **data\_index** ( _int32_)

- **value** ( _float_)



---

**set_default_custom_primitive_data_float_array**( _data_index_, _values_) → `None`

Set default custom primitive data, an array floats at once, from index DataIndex to index DataIndex + Values.Num(), and marks the render state dirty

Parameters:

- **data\_index** ( _int32_)

- **values** ( _Array_ _\_ [_float_ _]_)



---

**set_default_custom_primitive_data_vector2**( _data_index_, _value_) → `None`

Set default custom primitive data, two floats at once, from index DataIndex to index DataIndex + 1, and marks the render state dirty

Parameters:

- **data\_index** ( _int32_)

- **value** ( _Vector2D_)



---

**set_default_custom_primitive_data_vector3**( _data_index_, _value_) → `None`

Set default custom primitive data, three floats at once, from index DataIndex to index DataIndex + 2, and marks the render state dirty

Parameters:

- **data\_index** ( _int32_)

- **value** ( _Vector_)



---

**set_default_custom_primitive_data_vector4**( _data_index_, _value_) → `None`

Set default custom primitive data, four floats at once, from index DataIndex to index DataIndex + 3, and marks the render state dirty

Parameters:

- **data\_index** ( _int32_)

- **value** ( _Vector4_)



---

**set_emissive_light_source**( _new_emissive_light_source_) → `None`

Changes the value of EmissiveLightSource.

Parameters:

**new\_emissive\_light\_source** ( _bool_)


---

**set_enable_gravity**( _gravity_enabled_) → `None`

Enables/disables whether this component is affected by gravity. This applies only to components with bSimulatePhysics set to true.

Parameters:

**gravity\_enabled** ( _bool_)


---

**set_exclude_from_light_attachment_group**( _exclude_from_light_attachment_group_) → `None`

Changes the value of ExcludeFromLightAttachmentGroup.

Parameters:

**exclude\_from\_light\_attachment\_group** ( _bool_)


---

**set_excluded_from_hlod_level**( _hlod_level_, _excluded_) → `None`

Exclude this primitive from the specified HLOD level

Parameters:

- **hlod\_level** ( _HLODLevelExclusion_)

- **excluded** ( _bool_)



---

**set_first_person_primitive_type**( _value_) → `None`

Sets FirstPersonPrimitiveType property and marks the render state dirty.

Parameters:

**value** ( _FirstPersonPrimitiveType_)


---

**set_gyroscopic_torque_enabled**( _gyroscopic_torque_enabled_) → `None`

Enabled/disables whether this body is affected by gyroscopic torque, mainly useful for long/thin objects that spin

Parameters:

**gyroscopic\_torque\_enabled** ( _bool_)


---

**set_hidden_in_scene_capture**( _value_) → `None`

Sets bHideInSceneCapture property and marks the render state dirty.

Parameters:

**value** ( _bool_)


---

**set_holdout**( _new_holdout_) → `None`

Changes the value of bHoldout

Parameters:

**new\_holdout** ( _bool_)


---

**set_ignore_bounds_for_editor_focus**( _ignore_) → `None`

Set if we should ignore bounds when focusing the editor camera.

Parameters:

**ignore** ( _bool_)


---

**set_light_attachments_as_group**( _light_attachments_as_group_) → `None`

Changes the value of LightAttachmentsAsGroup.

Parameters:

**light\_attachments\_as\_group** ( _bool_)


---

**set_lighting_channels**( _channel0_, _channel1_, _channel2_) → `None`

Set Lighting Channels

Parameters:

- **channel0** ( _bool_)

- **channel1** ( _bool_)

- **channel2** ( _bool_)



---

**set_linear_damping**( _damping_) → `None`

Sets the linear damping of this component.

Parameters:

**damping** ( _float_)


---

**set_mass_override_in_kg**( _bone_name='None'_, _mass_in_kg=1.000000_, _override_mass=True_) → `None`

Override the mass (in Kg) of a single physics body.
Note that in the case where multiple bodies are attached together, the override mass will be set for the entire group.
Set the Override Mass to false if you want to reset the body’s mass to the auto-calculated physx mass.

Parameters:

- **bone\_name** ( _Name_)

- **mass\_in\_kg** ( _float_)

- **override\_mass** ( _bool_)



---

**set_mass_scale**( _bone_name='None'_, _mass_scale=1.000000_) → `None`

Change the mass scale used to calculate the mass of a single physics body

Parameters:

- **bone\_name** ( _Name_)

- **mass\_scale** ( _float_)



---

**set_material**( _element_index_, _material_) → `None`

Changes the material applied to an element of the mesh.

Parameters:

- **element\_index** ( _int32_) – The element to access the material of.

- **material** ( _MaterialInterface_)



---

**set_material_by_name**( _material_slot_name_, _material_) → `None`

Changes the material applied to an element of the mesh.

Parameters:

- **material\_slot\_name** ( _Name_) – The slot name to access the material of.

- **material** ( _MaterialInterface_)



---

**set_max_depenetration_velocity**( _bone_name='None'_, _max_depenetration_velocity=-1.000000_) → `None`

The maximum velocity used to depenetrate this object from others when spawned or teleported with initial overlaps (does not affect overlaps as a result of normal movement).
A value of zero will allow objects that are spawned overlapping to go to sleep without moving rather than pop out of each other. E.g., use zero if you spawn dynamic rocks
partially embedded in the ground and want them to be interactive but not pop out of the ground when touched.
A negative value means that the config setting CollisionInitialOverlapDepenetrationVelocity will be used.

Parameters:

- **bone\_name** ( _Name_)

- **max\_depenetration\_velocity** ( _float_)



---

**set_movement_channel**( _channel:CollisionChannel_) → `None`

deprecated: ‘set\_movement\_channel’ was renamed to ‘set\_collision\_object\_type’.


---

**set_notify_rigid_body_collision**( _new_notify_rigid_body_collision_) → `None`

Changes the value of bNotifyRigidBodyCollision

Parameters:

**new\_notify\_rigid\_body\_collision** ( _bool_)


---

**set_only_owner_see**( _new_only_owner_see_) → `None`

Changes the value of bOnlyOwnerSee.

Parameters:

**new\_only\_owner\_see** ( _bool_)


---

**set_owner_no_see**( _new_owner_no_see_) → `None`

Changes the value of bOwnerNoSee.

Parameters:

**new\_owner\_no\_see** ( _bool_)


---

**set_phys_material_override**( _new_phys_material_) → `None`

Changes the current PhysMaterialOverride for this component.
Note that if physics is already running on this component, this will \_not\_ alter its mass/inertia etc,
it will only change its surface properties like friction.

Parameters:

**new\_phys\_material** ( _PhysicalMaterial_)


---

**set_physics_angular_velocity_in_degrees**( _new_ang_vel_, _add_to_current=False_, _bone_name='None'_) → `None`

Set the angular velocity of a single body.
This should be used cautiously - it may be better to use AddTorque or AddImpulse.

Parameters:

- **new\_ang\_vel** ( _Vector_) – New angular velocity to apply to body, in degrees per second.

- **add\_to\_current** ( _bool_) – If true, NewAngVel is added to the existing angular velocity of the body.

- **bone\_name** ( _Name_) – If a SkeletalMeshComponent, name of body to modify angular velocity of. ‘None’ indicates root body.



---

**set_physics_angular_velocity_in_radians**( _new_ang_vel_, _add_to_current=False_, _bone_name='None'_) → `None`

Set the angular velocity of a single body.
This should be used cautiously - it may be better to use AddTorque or AddImpulse.

Parameters:

- **new\_ang\_vel** ( _Vector_) – New angular velocity to apply to body, in radians per second.

- **add\_to\_current** ( _bool_) – If true, NewAngVel is added to the existing angular velocity of the body.

- **bone\_name** ( _Name_) – If a SkeletalMeshComponent, name of body to modify angular velocity of. ‘None’ indicates root body.



---

**set_physics_linear_velocity**( _new_vel_, _add_to_current=False_, _bone_name='None'_) → `None`

Set the linear velocity of a single body.
This should be used cautiously - it may be better to use AddForce or AddImpulse.

Parameters:

- **new\_vel** ( _Vector_) – New linear velocity to apply to physics.

- **add\_to\_current** ( _bool_) – If true, NewVel is added to the existing velocity of the body.

- **bone\_name** ( _Name_) – If a SkeletalMeshComponent, name of body to modify velocity of. ‘None’ indicates root body.



---

**set_physics_max_angular_velocity_in_degrees**( _new_max_ang_vel_, _add_to_current=False_, _bone_name='None'_) → `None`

Set the maximum angular velocity of a single body.

Parameters:

- **new\_max\_ang\_vel** ( _float_) – New maximum angular velocity to apply to body, in degrees per second.

- **add\_to\_current** ( _bool_) – If true, NewMaxAngVel is added to the existing maximum angular velocity of the body.

- **bone\_name** ( _Name_) – If a SkeletalMeshComponent, name of body to modify maximum angular velocity of. ‘None’ indicates root body.



---

**set_physics_max_angular_velocity_in_radians**( _new_max_ang_vel_, _add_to_current=False_, _bone_name='None'_) → `None`

Set the maximum angular velocity of a single body.

Parameters:

- **new\_max\_ang\_vel** ( _float_) – New maximum angular velocity to apply to body, in radians per second.

- **add\_to\_current** ( _bool_) – If true, NewMaxAngVel is added to the existing maximum angular velocity of the body.

- **bone\_name** ( _Name_) – If a SkeletalMeshComponent, name of body to modify maximum angular velocity of. ‘None’ indicates root body.



---

**set_rb_linear_velocity**( _new_vel:Vector_, _add_to_current:bool=False_, _bone_name:Name='None'_) → `None`

deprecated: ‘set\_rb\_linear\_velocity’ was renamed to ‘set\_physics\_linear\_velocity’.


---

**set_receives_decals**( _new_receives_decals_) → `None`

Changes the value of bReceivesDecals.

Parameters:

**new\_receives\_decals** ( _bool_)


---

**set_render_custom_depth**( _value_) → `None`

Sets the bRenderCustomDepth property and marks the render state dirty.

Parameters:

**value** ( _bool_)


---

**set_render_in_depth_pass**( _value_) → `None`

Sets bRenderInDepthPass property and marks the render state dirty.

Parameters:

**value** ( _bool_)


---

**set_render_in_main_pass**( _value_) → `None`

Sets bRenderInMainPass property and marks the render state dirty.

Parameters:

**value** ( _bool_)


---

**set_scalar_parameter_for_custom_primitive_data**( _parameter_name_, _value_) → `None`

Set a scalar parameter for custom primitive data. This sets the run-time data only, so it doesn’t serialize.

Parameters:

- **parameter\_name** ( _Name_) – The parameter name of the custom primitive

- **value** ( _float_) – The new value of the custom primitive



---

**set_scalar_parameter_for_default_custom_primitive_data**( _parameter_name_, _value_) → `None`

Set a scalar parameter for default custom primitive data. This will be serialized and is useful in construction scripts.

Parameters:

- **parameter\_name** ( _Name_) – The parameter name of the custom primitive

- **value** ( _float_) – The new value of the custom primitive



---

**set_simulate_physics**( _simulate_) → `None`

When this component is a simple/single body, this will enable or disable simulation on that body. In addition,
if this component is currently attached to something, beginning simulation will detach it. Note that stopping
simulation will not reattach the component - that would need to be done explicitly.

For more complex components (e.g. skeletal meshes), simulation will apply to the bodies contained by the
component (e.g. using a physics asset). Since these bodies will be free to move independently of the component,
the component will not be automatically detached. If detachment is required, then that can be done by
calling DetachFromComponent.

Parameters:

**simulate** ( _bool_) – New simulation state for the single body or multiple bodies


---

**set_single_sample_shadow_from_stationary_lights**( _new_single_sample_shadow_from_stationary_lights_) → `None`

Changes the value of bSingleSampleShadowFromStationaryLights.

Parameters:

**new\_single\_sample\_shadow\_from\_stationary\_lights** ( _bool_)


---

**set_static_when_not_moveable**( _static_when_not_moveable_) → `None`

Set Static when Not Moveable

Parameters:

**static\_when\_not\_moveable** ( _bool_)


---

**set_translucency_sort_distance_offset**( _new_translucency_sort_distance_offset_) → `None`

Changes the value of TranslucencySortDistanceOffset.

Parameters:

**new\_translucency\_sort\_distance\_offset** ( _float_)


---

**set_translucent_sort_priority**( _new_translucent_sort_priority_) → `None`

Changes the value of TranslucentSortPriority.

Parameters:

**new\_translucent\_sort\_priority** ( _int32_)


---

**set_update_kinematic_from_simulation**( _update_kinematic_from_simulation_) → `None`

Enables/disables whether this component should be updated by simulation when it is kinematic. This is needed if (for example) its velocity needs to be accessed.

Parameters:

**update\_kinematic\_from\_simulation** ( _bool_)


---

**set_use_ccd**( _use_ccd_, _bone_name='None'_) → `None`

Set whether this component should use Continuous Collision Detection

Parameters:

- **use\_ccd** ( _bool_)

- **bone\_name** ( _Name_)



---

**set_use_macd**( _use_macd_, _bone_name='None'_) → `None`

[EXPERIMENTAL] Set whether this component should use Motion-Aware Collision Detection

Parameters:

- **use\_macd** ( _bool_)

- **bone\_name** ( _Name_)



---

**set_vector_parameter_for_custom_primitive_data**( _parameter_name_, _value_) → `None`

Set a vector parameter for custom primitive data. This sets the run-time data only, so it doesn’t serialize.

Parameters:

- **parameter\_name** ( _Name_) – The parameter name of the custom primitive

- **value** ( _Vector4_) – The new value of the custom primitive



---

**set_vector_parameter_for_default_custom_primitive_data**( _parameter_name_, _value_) → `None`

Set a vector parameter for default custom primitive data. This will be serialized and is useful in construction scripts.

Parameters:

- **parameter\_name** ( _Name_) – The parameter name of the custom primitive

- **value** ( _Vector4_) – The new value of the custom primitive



---

**set_visible_in_ray_tracing**( _new_visible_in_ray_tracing_) → `None`

Changes the value of bIsVisibleInRayTracing.

Parameters:

**new\_visible\_in\_ray\_tracing** ( _bool_)


---

**set_visible_in_scene_capture_only**( _value_) → `None`

Sets bVisibleInSceneCaptureOnly property and marks the render state dirty.

Parameters:

**value** ( _bool_)


---

**set_walkable_slope_override**( _new_override_) → `None`

Sets a new slope override for this component instance.

Parameters:

**new\_override** ( _WalkableSlopeOverride_)


---

_property_ `shadow_cache_invalidation_behavior`: ShadowCacheInvalidationBehavior

[Read-Only] Control shadow invalidation behavior, in particular with respect to Virtual Shadow Maps and material effects like World Position Offset.

**Type:**

( ShadowCacheInvalidationBehavior)


---

_property_ `single_sample_shadow_from_stationary_lights`: bool

[Read-Only] Whether the whole component should be shadowed as one from stationary lights, which makes shadow receiving much cheaper.
When enabled shadowing data comes from the volume lighting samples precomputed by Lightmass, which are very sparse.
This is currently only used on stationary directional lights.

**Type:**

( bool)


---

**sphere_overlap_component**( _sphere_centre_, _sphere_radius_, _trace_complex=True_, _show_trace_, _persistent_show_trace=False_) → `(hit_location=Vector,hit_normal=Vector,bone_name=Name,out_hit=HitResult)orNone`

Perform a sphere overlap against a single component

Parameters:

- **sphere\_centre** ( _Vector_) – The centre of the sphere to overlap with the component

- **sphere\_radius** ( _float_) – The Radius of the sphere to overlap with the component

- **trace\_complex** ( _bool_) – Whether or not to trace the complex physics representation or just the simple representation

- **show\_trace** ( _bool_) – Whether or not to draw the trace in the world (for debugging)

- **persistent\_show\_trace** ( _bool_) – Whether or not to make the debugging draw stay in the world permanently


Returns:

hit\_location (Vector):

hit\_normal (Vector):

bone\_name (Name):

out\_hit (HitResult):

Return type:

tuple or None


---

**sphere_trace_component**( _trace_start_, _trace_end_, _sphere_radius_, _trace_complex=True_, _show_trace_, _persistent_show_trace=False_) → `(hit_location=Vector,hit_normal=Vector,bone_name=Name,out_hit=HitResult)orNone`

Perform a sphere trace against a single component

Parameters:

- **trace\_start** ( _Vector_) – The start of the trace in world-space

- **trace\_end** ( _Vector_) – The end of the trace in world-space

- **sphere\_radius** ( _float_) – Radius of the sphere to trace against the component

- **trace\_complex** ( _bool_) – Whether or not to trace the complex physics representation or just the simple representation

- **show\_trace** ( _bool_) – Whether or not to draw the trace in the world (for debugging)

- **persistent\_show\_trace** ( _bool_) – Whether or not to make the debugging draw stay in the world permanently


Returns:

hit\_location (Vector):

hit\_normal (Vector):

bone\_name (Name):

out\_hit (HitResult):

Return type:

tuple or None


---

_property_ `static_when_not_moveable`: bool

[Read-Only] When false, the underlying physics body will contain all sim data (mass, inertia tensor, etc) even if mobility is not set to Moveable

**Type:**

( bool)


---

_property_ `trace_complex_on_move`: bool

[Read-Write] If true, component sweeps with this component should trace against complex collision during movement (for example, each triangle of a mesh).
If false, collision will be resolved against simple collision bounds instead.
see: MoveComponent()

**Type:**

( bool)


---

_property_ `translucency_sort_distance_offset`: float

[Read-Only] Modified sort distance offset for translucent objects in world units.
A positive number will move the sort distance further and a negative number will move the distance closer.

Ignored if the object is not translucent.
Warning: Adjusting this value will prevent the renderer from correctly sorting based on distance. Only modify this value if you are certain it will not cause visual artifacts.

**Type:**

( float)


---

_property_ `translucency_sort_priority`: int

[Read-Only] Translucent objects with a lower sort priority draw behind objects with a higher priority.
Translucent objects with the same priority are rendered from back-to-front based on their bounds origin.
This setting is also used to sort objects being drawn into a runtime virtual texture.

Ignored if the object is not translucent. The default priority is zero.
Warning: This should never be set to a non-default value unless you know what you are doing, as it will prevent the renderer from sorting correctly.
It is especially problematic on dynamic gameplay effects.

**Type:**

(int32)


---

_property_ `treat_as_background_for_occlusion`: bool

[Read-Only] Treat this primitive as part of the background for occlusion purposes. This can be used as an optimization to reduce the cost of rendering skyboxes, large ground planes that are part of the vista, etc.

**Type:**

( bool)


---

**unregister_as_focal_point_in_physics_replication_lod**() → `None`

Unregister this components physics object from being a focal particle in Physics Replication LOD


---

_property_ `use_as_occluder`: bool

[Read-Only] Whether to render the primitive in the depth only pass.
This should generally be true for all objects, and let the renderer make decisions about whether to render objects in the depth only pass.
todo: if any rendering features rely on a complete depth only pass, this variable needs to go away.

**Type:**

( bool)


---

_property_ `virtual_texture_render_pass_type`: RuntimeVirtualTextureMainPassType

[Read-Write] Controls if this component draws in the main pass as well as in the virtual texture.

**Type:**

( RuntimeVirtualTextureMainPassType)


---

_property_ `visible_in_ray_tracing`: bool

[Read-Only] If true, this component will be visible in ray tracing effects. Turning this off will remove it from ray traced reflections, shadows, etc.

**Type:**

( bool)


---

_property_ `visible_in_real_time_sky_captures`: bool

[Read-Only] If true, this component will be visible in real-time sky light reflection captures.

**Type:**

( bool)


---

_property_ `visible_in_reflection_captures`: bool

[Read-Only] If true, this component will be visible in reflection captures.

**Type:**

( bool)


---

_property_ `visible_in_scene_capture_only`: bool

[Read-Only] When true, will only be visible in Scene Capture

**Type:**

( bool)


---

**wake_all_rigid_bodies**() → `None`

Ensure simulation is running for all bodies in this component.


---

**wake_rigid_body**( _bone_name='None'_) → `None`

‘Wake’ physics simulation for a single body.

Parameters:

**bone\_name** ( _Name_) – If a SkeletalMeshComponent, name of body to wake. ‘None’ indicates root body.


---

**was_recently_rendered**( _tolerance=0.200000_) → `bool`

Returns true if this component has been rendered “recently”, with a tolerance in seconds to define what “recent” means.
e.g.: If a tolerance of 0.1 is used, this function will return true only if the actor was rendered in the last 0.1 seconds of game time.

Parameters:

**tolerance** ( _float_) – How many seconds ago the actor last render time can be and still count as having been “recently” rendered.

Returns:

Whether this actor was recently rendered.

Return type:

bool

### Table of Contents

- `unreal.PrimitiveComponent`
  - `PrimitiveComponent`
    - `PrimitiveComponent.add_angular_impulse_in_degrees()`
    - `PrimitiveComponent.add_angular_impulse_in_radians()`
    - `PrimitiveComponent.add_force()`
    - `PrimitiveComponent.add_force_at_location()`
    - `PrimitiveComponent.add_force_at_location_local()`
    - `PrimitiveComponent.add_force_at_position()`
    - `PrimitiveComponent.add_impulse()`
    - `PrimitiveComponent.add_impulse_at_location()`
    - `PrimitiveComponent.add_impulse_at_position()`
    - `PrimitiveComponent.add_radial_force()`
    - `PrimitiveComponent.add_radial_impulse()`
    - `PrimitiveComponent.add_torque_in_degrees()`
    - `PrimitiveComponent.add_torque_in_radians()`
    - `PrimitiveComponent.add_velocity_change_impulse_at_location()`
    - `PrimitiveComponent.affect_distance_field_lighting`
    - `PrimitiveComponent.affect_dynamic_indirect_lighting`
    - `PrimitiveComponent.affect_indirect_lighting_while_hidden`
    - `PrimitiveComponent.allow_cull_distance_volume`
    - `PrimitiveComponent.always_create_physics_state`
    - `PrimitiveComponent.apply_impulse_on_damage`
    - `PrimitiveComponent.body_instance`
    - `PrimitiveComponent.box_overlap_component()`
    - `PrimitiveComponent.cached_max_draw_distance`
    - `PrimitiveComponent.can_be_character_base`
    - `PrimitiveComponent.can_character_step_up()`
    - `PrimitiveComponent.can_character_step_up_on`
    - `PrimitiveComponent.cast_cinematic_shadow`
    - `PrimitiveComponent.cast_contact_shadow`
    - `PrimitiveComponent.cast_dynamic_shadow`
    - `PrimitiveComponent.cast_far_shadow`
    - `PrimitiveComponent.cast_hidden_shadow`
    - `PrimitiveComponent.cast_inset_shadow`
    - `PrimitiveComponent.cast_shadow`
    - `PrimitiveComponent.cast_shadow_as_two_sided`
    - `PrimitiveComponent.cast_static_shadow`
    - `PrimitiveComponent.cast_volumetric_translucent_shadow`
    - `PrimitiveComponent.clear_move_ignore_actors()`
    - `PrimitiveComponent.clear_move_ignore_components()`
    - `PrimitiveComponent.copy_array_of_move_ignore_actors()`
    - `PrimitiveComponent.copy_array_of_move_ignore_components()`
    - `PrimitiveComponent.create_and_set_material_instance_dynamic()`
    - `PrimitiveComponent.create_and_set_material_instance_dynamic_from_material()`
    - `PrimitiveComponent.create_dynamic_material_instance()`
    - `PrimitiveComponent.custom_depth_stencil_value`
    - `PrimitiveComponent.custom_depth_stencil_write_mask`
    - `PrimitiveComponent.emissive_light_source`
    - `PrimitiveComponent.enable_auto_lod_generation`
    - `PrimitiveComponent.exclude_for_specific_hlod_levels`
    - `PrimitiveComponent.exclude_from_light_attachment_group`
    - `PrimitiveComponent.first_person_primitive_type`
    - `PrimitiveComponent.force_mip_streaming`
    - `PrimitiveComponent.generate_overlap_events`
    - `PrimitiveComponent.get_angular_damping()`
    - `PrimitiveComponent.get_body_instance_async_physics_tick_handle()`
    - `PrimitiveComponent.get_center_of_mass()`
    - `PrimitiveComponent.get_closest_point_on_collision()`
    - `PrimitiveComponent.get_collision_enabled()`
    - `PrimitiveComponent.get_collision_object_type()`
    - `PrimitiveComponent.get_collision_profile_name()`
    - `PrimitiveComponent.get_collision_response_to_channel()`
    - `PrimitiveComponent.get_custom_primitive_data_index_for_scalar_parameter()`
    - `PrimitiveComponent.get_custom_primitive_data_index_for_vector_parameter()`
    - `PrimitiveComponent.get_editor_material()`
    - `PrimitiveComponent.get_gyroscopic_torque_enabled()`
    - `PrimitiveComponent.get_ignore_bounds_for_editor_focus()`
    - `PrimitiveComponent.get_inertia_tensor()`
    - `PrimitiveComponent.get_linear_damping()`
    - `PrimitiveComponent.get_mass()`
    - `PrimitiveComponent.get_mass_scale()`
    - `PrimitiveComponent.get_material()`
    - `PrimitiveComponent.get_material_by_name()`
    - `PrimitiveComponent.get_material_from_collision_face_index()`
    - `PrimitiveComponent.get_material_index()`
    - `PrimitiveComponent.get_material_slot_names()`
    - `PrimitiveComponent.get_max_depenetration_velocity()`
    - `PrimitiveComponent.get_move_ignore_actors()`
    - `PrimitiveComponent.get_num_materials()`
    - `PrimitiveComponent.get_overlapping_actors()`
    - `PrimitiveComponent.get_overlapping_components()`
    - `PrimitiveComponent.get_physics_angular_velocity_in_degrees()`
    - `PrimitiveComponent.get_physics_angular_velocity_in_radians()`
    - `PrimitiveComponent.get_physics_linear_velocity()`
    - `PrimitiveComponent.get_physics_linear_velocity_at_point()`
    - `PrimitiveComponent.get_rb_linear_velocity()`
    - `PrimitiveComponent.get_static_when_not_moveable()`
    - `PrimitiveComponent.get_touching_actors()`
    - `PrimitiveComponent.get_touching_components()`
    - `PrimitiveComponent.get_update_kinematic_from_simulation()`
    - `PrimitiveComponent.get_walkable_slope_override()`
    - `PrimitiveComponent.has_per_instance_hit_proxies`
    - `PrimitiveComponent.hidden_in_scene_capture`
    - `PrimitiveComponent.hlod_batching_policy`
    - `PrimitiveComponent.holdout`
    - `PrimitiveComponent.ignore_actor_when_moving()`
    - `PrimitiveComponent.ignore_component_when_moving()`
    - `PrimitiveComponent.ignore_radial_force`
    - `PrimitiveComponent.ignore_radial_impulse`
    - `PrimitiveComponent.indirect_lighting_cache_quality`
    - `PrimitiveComponent.invalidate_lumen_surface_cache()`
    - `PrimitiveComponent.is_any_rigid_body_awake()`
    - `PrimitiveComponent.is_collision_enabled()`
    - `PrimitiveComponent.is_excluded_from_hlod_level()`
    - `PrimitiveComponent.is_gravity_enabled()`
    - `PrimitiveComponent.is_material_slot_name_valid()`
    - `PrimitiveComponent.is_overlapping_actor()`
    - `PrimitiveComponent.is_overlapping_component()`
    - `PrimitiveComponent.is_physics_collision_enabled()`
    - `PrimitiveComponent.is_query_collision_enabled()`
    - `PrimitiveComponent.ld_max_draw_distance`
    - `PrimitiveComponent.light_attachments_as_group`
    - `PrimitiveComponent.lighting_channels`
    - `PrimitiveComponent.lightmap_type`
    - `PrimitiveComponent.line_trace_component()`
    - `PrimitiveComponent.min_draw_distance`
    - `PrimitiveComponent.multi_body_overlap`
    - `PrimitiveComponent.never_distance_cull`
    - `PrimitiveComponent.on_begin_cursor_over`
    - `PrimitiveComponent.on_clicked`
    - `PrimitiveComponent.on_component_begin_overlap`
    - `PrimitiveComponent.on_component_end_overlap`
    - `PrimitiveComponent.on_component_hit`
    - `PrimitiveComponent.on_component_physics_state_changed`
    - `PrimitiveComponent.on_component_sleep`
    - `PrimitiveComponent.on_component_wake`
    - `PrimitiveComponent.on_end_cursor_over`
    - `PrimitiveComponent.on_input_touch_begin`
    - `PrimitiveComponent.on_input_touch_end`
    - `PrimitiveComponent.on_input_touch_enter`
    - `PrimitiveComponent.on_input_touch_leave`
    - `PrimitiveComponent.on_released`
    - `PrimitiveComponent.only_owner_see`
    - `PrimitiveComponent.owner_no_see`
    - `PrimitiveComponent.put_rigid_body_to_sleep()`
    - `PrimitiveComponent.ray_tracing_group_culling_priority`
    - `PrimitiveComponent.ray_tracing_group_id`
    - `PrimitiveComponent.receive_mobile_csm_shadows`
    - `PrimitiveComponent.receives_decals`
    - `PrimitiveComponent.register_as_focal_point_in_physics_replication_lod()`
    - `PrimitiveComponent.render_custom_depth`
    - `PrimitiveComponent.render_in_depth_pass`
    - `PrimitiveComponent.render_in_main_pass`
    - `PrimitiveComponent.replicate_physics_to_autonomous_proxy`
    - `PrimitiveComponent.return_material_on_move`
    - `PrimitiveComponent.runtime_virtual_textures`
    - `PrimitiveComponent.scale_by_moment_of_inertia()`
    - `PrimitiveComponent.self_shadow_only`
    - `PrimitiveComponent.set_affect_distance_field_lighting()`
    - `PrimitiveComponent.set_affect_dynamic_indirect_lighting()`
    - `PrimitiveComponent.set_affect_indirect_lighting_while_hidden()`
    - `PrimitiveComponent.set_all_allow_partial_island_sleep()`
    - `PrimitiveComponent.set_all_mass_scale()`
    - `PrimitiveComponent.set_all_physics_angular_velocity_in_degrees()`
    - `PrimitiveComponent.set_all_physics_angular_velocity_in_radians()`
    - `PrimitiveComponent.set_all_physics_linear_velocity()`
    - `PrimitiveComponent.set_all_rb_linear_velocity()`
    - `PrimitiveComponent.set_all_use_ccd()`
    - `PrimitiveComponent.set_all_use_macd()`
    - `PrimitiveComponent.set_allow_partial_island_sleep()`
    - `PrimitiveComponent.set_angular_damping()`
    - `PrimitiveComponent.set_bounds_scale()`
    - `PrimitiveComponent.set_cast_contact_shadow()`
    - `PrimitiveComponent.set_cast_hidden_shadow()`
    - `PrimitiveComponent.set_cast_inset_shadow()`
    - `PrimitiveComponent.set_cast_shadow()`
    - `PrimitiveComponent.set_center_of_mass()`
    - `PrimitiveComponent.set_collision_enabled()`
    - `PrimitiveComponent.set_collision_object_type()`
    - `PrimitiveComponent.set_collision_profile_name()`
    - `PrimitiveComponent.set_collision_response_to_all_channels()`
    - `PrimitiveComponent.set_collision_response_to_channel()`
    - `PrimitiveComponent.set_constraint_mode()`
    - `PrimitiveComponent.set_cull_distance()`
    - `PrimitiveComponent.set_custom_depth_stencil_value()`
    - `PrimitiveComponent.set_custom_depth_stencil_write_mask()`
    - `PrimitiveComponent.set_custom_primitive_data_float()`
    - `PrimitiveComponent.set_custom_primitive_data_float_array()`
    - `PrimitiveComponent.set_custom_primitive_data_vector2()`
    - `PrimitiveComponent.set_custom_primitive_data_vector3()`
    - `PrimitiveComponent.set_custom_primitive_data_vector4()`
    - `PrimitiveComponent.set_default_custom_primitive_data_float()`
    - `PrimitiveComponent.set_default_custom_primitive_data_float_array()`
    - `PrimitiveComponent.set_default_custom_primitive_data_vector2()`
    - `PrimitiveComponent.set_default_custom_primitive_data_vector3()`
    - `PrimitiveComponent.set_default_custom_primitive_data_vector4()`
    - `PrimitiveComponent.set_emissive_light_source()`
    - `PrimitiveComponent.set_enable_gravity()`
    - `PrimitiveComponent.set_exclude_from_light_attachment_group()`
    - `PrimitiveComponent.set_excluded_from_hlod_level()`
    - `PrimitiveComponent.set_first_person_primitive_type()`
    - `PrimitiveComponent.set_gyroscopic_torque_enabled()`
    - `PrimitiveComponent.set_hidden_in_scene_capture()`
    - `PrimitiveComponent.set_holdout()`
    - `PrimitiveComponent.set_ignore_bounds_for_editor_focus()`
    - `PrimitiveComponent.set_light_attachments_as_group()`
    - `PrimitiveComponent.set_lighting_channels()`
    - `PrimitiveComponent.set_linear_damping()`
    - `PrimitiveComponent.set_mass_override_in_kg()`
    - `PrimitiveComponent.set_mass_scale()`
    - `PrimitiveComponent.set_material()`
    - `PrimitiveComponent.set_material_by_name()`
    - `PrimitiveComponent.set_max_depenetration_velocity()`
    - `PrimitiveComponent.set_movement_channel()`
    - `PrimitiveComponent.set_notify_rigid_body_collision()`
    - `PrimitiveComponent.set_only_owner_see()`
    - `PrimitiveComponent.set_owner_no_see()`
    - `PrimitiveComponent.set_phys_material_override()`
    - `PrimitiveComponent.set_physics_angular_velocity_in_degrees()`
    - `PrimitiveComponent.set_physics_angular_velocity_in_radians()`
    - `PrimitiveComponent.set_physics_linear_velocity()`
    - `PrimitiveComponent.set_physics_max_angular_velocity_in_degrees()`
    - `PrimitiveComponent.set_physics_max_angular_velocity_in_radians()`
    - `PrimitiveComponent.set_rb_linear_velocity()`
    - `PrimitiveComponent.set_receives_decals()`
    - `PrimitiveComponent.set_render_custom_depth()`
    - `PrimitiveComponent.set_render_in_depth_pass()`
    - `PrimitiveComponent.set_render_in_main_pass()`
    - `PrimitiveComponent.set_scalar_parameter_for_custom_primitive_data()`
    - `PrimitiveComponent.set_scalar_parameter_for_default_custom_primitive_data()`
    - `PrimitiveComponent.set_simulate_physics()`
    - `PrimitiveComponent.set_single_sample_shadow_from_stationary_lights()`
    - `PrimitiveComponent.set_static_when_not_moveable()`
    - `PrimitiveComponent.set_translucency_sort_distance_offset()`
    - `PrimitiveComponent.set_translucent_sort_priority()`
    - `PrimitiveComponent.set_update_kinematic_from_simulation()`
    - `PrimitiveComponent.set_use_ccd()`
    - `PrimitiveComponent.set_use_macd()`
    - `PrimitiveComponent.set_vector_parameter_for_custom_primitive_data()`
    - `PrimitiveComponent.set_vector_parameter_for_default_custom_primitive_data()`
    - `PrimitiveComponent.set_visible_in_ray_tracing()`
    - `PrimitiveComponent.set_visible_in_scene_capture_only()`
    - `PrimitiveComponent.set_walkable_slope_override()`
    - `PrimitiveComponent.shadow_cache_invalidation_behavior`
    - `PrimitiveComponent.single_sample_shadow_from_stationary_lights`
    - `PrimitiveComponent.sphere_overlap_component()`
    - `PrimitiveComponent.sphere_trace_component()`
    - `PrimitiveComponent.static_when_not_moveable`
    - `PrimitiveComponent.trace_complex_on_move`
    - `PrimitiveComponent.translucency_sort_distance_offset`
    - `PrimitiveComponent.translucency_sort_priority`
    - `PrimitiveComponent.treat_as_background_for_occlusion`
    - `PrimitiveComponent.unregister_as_focal_point_in_physics_replication_lod()`
    - `PrimitiveComponent.use_as_occluder`
    - `PrimitiveComponent.virtual_texture_render_pass_type`
    - `PrimitiveComponent.visible_in_ray_tracing`
    - `PrimitiveComponent.visible_in_real_time_sky_captures`
    - `PrimitiveComponent.visible_in_reflection_captures`
    - `PrimitiveComponent.visible_in_scene_capture_only`
    - `PrimitiveComponent.wake_all_rigid_bodies()`
    - `PrimitiveComponent.wake_rigid_body()`
    - `PrimitiveComponent.was_recently_rendered()`