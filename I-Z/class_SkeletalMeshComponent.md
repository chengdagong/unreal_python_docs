# unreal.SkeletalMeshComponent

```python
class unreal.SkeletalMeshComponent(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``SkinnedMeshComponent``


SkeletalMeshComponent is used to create an instance of an animated SkeletalMesh asset.
see: https://docs.unrealengine.com/latest/INT/Engine/Content/Types/SkeletalMeshes/
see: USkeletalMesh

**C++ Source:**

- **Module**: Engine

- **File**: SkeletalMeshComponent.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `absolute_location` (bool): [Read-Write] If RelativeLocation should be considered relative to the world, rather than the parent

- `absolute_rotation` (bool): [Read-Write] If RelativeRotation should be considered relative to the world, rather than the parent

- `absolute_scale` (bool): [Read-Write] If RelativeScale3D should be considered relative to the world, rather than the parent

- `affect_distance_field_lighting` (bool): [Read-Write] Controls whether the primitive should affect dynamic distance field lighting methods. This flag is only used if CastShadow is true.

- `affect_dynamic_indirect_lighting` (bool): [Read-Write] Controls whether the primitive should influence indirect lighting.

- `affect_indirect_lighting_while_hidden` (bool): [Read-Write] Controls whether the primitive should affect indirect lighting when hidden. This flag is only used if bAffectDynamicIndirectLighting is true.

- `allow_anim_curve_evaluation` (bool): [Read-Write] Disable animation curves for this component. If this is set true, no curves will be processed

- `allow_cloth_actors` (bool): [Read-Write] Toggles creation of cloth simulation. Distinct from the simulation toggle below in that, if off, avoids allocating
the actors entirely instead of just skipping the simulation step.

- `allow_cull_distance_volume` (bool): [Read-Write] Whether to accept cull distance volumes to modify cached cull distance.

- `always_create_physics_state` (bool): [Read-Write] Indicates if we’d like to create physics state all the time (for collision and simulation).
If you set this to false, it still will create physics state if collision or simulation activated.
This can help performance if you’d like to avoid overhead of creating physics state when triggers

- `always_use_mesh_deformer` (bool): [Read-Write] If true, and if no mesh deformer is set from here or the SkeletalMesh, fall back to the default deformer specified in the project settings, unless DefaultMode is set to “Never” in project settings

- `anim_blueprint_generated_class` (type(AnimBlueprintGeneratedClass)): [Read-Write]

- `anim_class` (type(Class)): [Read-Write] The AnimBlueprint class to use. Use ‘SetAnimInstanceClass’ to change at runtime.

- `animation_data` (SingleAnimationPlayData): [Read-Write]

- `animation_mode` (AnimationMode): [Read-Write] Whether to use Animation Blueprint or play Single Animation Asset.

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

- `capsule_indirect_shadow_min_visibility` (float): [Read-Write] Controls how dark the capsule indirect shadow can be.

- `cast_capsule_direct_shadow` (bool): [Read-Write] Whether to use the capsule representation (when present) from a skeletal mesh’s ShadowPhysicsAsset for direct shadowing from lights.
This type of shadowing is approximate but handles extremely wide area shadowing well. The softness of the shadow depends on the light’s LightSourceAngle / SourceRadius.
This flag will force bCastInsetShadow to be enabled. This flag is only used if CastShadow is true and if FirstPersonPrimitiveType is not set to FirstPerson.

- `cast_capsule_indirect_shadow` (bool): [Read-Write] Whether to use the capsule representation (when present) from a skeletal mesh’s ShadowPhysicsAsset for shadowing indirect lighting (from lightmaps or skylight).
This flag is only used if CastShadow is true and if FirstPersonPrimitiveType is not set to FirstPerson.

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

- `cloth_blend_weight` (float): [Read-Write] weight to blend between simulated results and key-framed positions
if weight is 1.0, shows only cloth simulation results and 0.0 will show only skinned results

- `cloth_geometry_scale` (float): [Read-Write] This scale is applied to all cloth geometry (e.g., cloth meshes and collisions) in order to simulate in a different scale space than world.This scale is not applied to distance-based simulation parameters such as MaxDistance.
This property is currently only read by the cloth solver when creating cloth actors, but may become animatable in the future.

- `cloth_max_distance_scale` (float): [Read-Write]

- `cloth_teleport_mode` (ClothingTeleportMode): [Read-Only] whether we need to teleport cloth. // This property is explicitly hidden from the details panel inside FSkeletalMeshComponentDetails::UpdatePhysicsCategory

- `cloth_velocity_scale` (float): [Read-Write] Scale applied to the component induced velocity of all cloth particles prior to stepping the cloth solver.
Use 1.0 for fully induced velocity (default), or use 0.0 for no induced velocity, and any other values in between for a reduced induced velocity.
When set to 0.0, it also provides a way to force the clothing to simulate in local space.
This value multiplies to individual cloth’s velocity scale settings, still allowing for differences in behavior between the various pieces of clothing within the same component.

- `collide_with_attached_children` (bool): [Read-Write] can’t collide with part of attached children if total collision volumes exceed 16 capsules or 32 planes per convex

- `collide_with_environment` (bool): [Read-Write] can’t collide with part of environment if total collision volumes exceed 16 capsules or 32 planes per convex

- `component_tags` (Array[Name]): [Read-Write] Array of tags that can be used for grouping and categorizing. Can also be accessed from scripting.

- `component_use_fixed_skel_bounds` (bool): [Read-Write] When true, skip using the physics asset etc. and always use the fixed bounds defined in the SkeletalMesh.

- `consider_all_bodies_for_bounds` (bool): [Read-Write] If true, when updating bounds from a PhysicsAsset, consider \_all\_ BodySetups, not just those flagged with bConsiderForBounds.

- `consider_for_actor_placement_when_hidden` (bool): [Read-Write] If true, this component will be considered for placement when dragging and placing items in the editor even if it is not visible, such as in the case of hidden collision meshes

- `custom_depth_stencil_value` (int32): [Read-Write] Optionally write this 0-255 value to the stencil buffer in CustomDepth pass (Requires project setting or r.CustomDepth == 3)

- `custom_depth_stencil_write_mask` (RendererStencilMask): [Read-Write] Mask used for stencil buffer writes.

- `custom_primitive_data` (CustomPrimitiveData): [Read-Write] Optional user defined default values for the custom primitive data of this primitive

- `default_animating_rig_override` (Object): [Read-Write] Default Animating Rig to Use if bOverrideDefaultAnimatingRig is true

- `defer_kinematic_bone_update` (bool): [Read-Write] Whether animation and world transform updates are deferred. If this is on, the kinematic bodies (scene query data) will not update until the next time the physics simulation is run

- `detail_mode` (DetailMode): [Read-Write] Set the required detail level of this component.
It will be deleted or made invisible if the world’s detail level is higher, based on platform and scalability settings.
For example, a detail mode of High may prevent this component from loading on mobile platforms.

- `disable_cloth_simulation` (bool): [Read-Write] Disable cloth simulation and play original animation without simulation

- `disable_morph_target` (bool): [Read-Write] Disable Morphtarget for this component.

- `disable_post_process_blueprint` (bool): [Read-Write] Controls whether or not this component will evaluate its post process instance. The post-process
Instance is dictated by the skeletal mesh so this is used for per-instance control.

- `disable_rigid_body_anim_node` (bool): [Read-Write] Disable rigid body animation nodes and play original animation without simulation

- `display_bones` (bool): [Read-Write] Draw the skeleton hierarchy for this skel mesh.

- `display_debug_update_rate_optimizations` (bool): [Read-Write] Enable on screen debugging of update rate optimization.
Red = Skipping 0 frames, Green = skipping 1 frame, Blue = skipping 2 frames, black = skipping more than 2 frames.
todo:: turn this into a console command.

- `editable_when_inherited` (bool): [Read-Write] True if this component can be modified when it was inherited from a parent actor class

- `emissive_light_source` (bool): [Read-Write] Whether the primitive will be used as an emissive light source.

- `enable_animation` (bool): [Read-Write] Whether the built-in animation of this component should run when the component ticks.
It is assumed that if this is false then some external system will be animating this mesh.
Note that disabling animation will also cause cloth simulation not to run and the component’s tick to run on any thread.

- `enable_auto_lod_generation` (bool): [Read-Write] Whether to include this component in HLODs or not.

- `enable_material_parameter_caching` (bool): [Read-Write] Whether or not to cache material parameter to speed up setting scalar or vector value on materials

- `enable_per_poly_collision` (bool): [Read-Write] Uses skinned data for collision data.

- `enable_physics_on_dedicated_server` (bool): [Read-Write] If true, simulate physics for this component on a dedicated server.
This should be set if simulating physics and replicating with a dedicated server.


> Note: This property cannot be changed at runtime.

- `enable_update_rate_optimizations` (bool): [Read-Write] if TRUE, Owner will determine how often animation will be updated and evaluated. See AnimUpdateRateTick()
This allows to skip frames for performance. (For example based on visibility and size on screen).

- `exclude_for_specific_hlod_levels` (Array[int32]): [Read-Write]
deprecated: WARNING: This property has been deprecated, use the SetExcludedFromHLODLevel/IsExcludedFromHLODLevel functions instead

- `exclude_from_hlod_levels` (uint8): [Read-Write] Which specific HLOD levels this component should be excluded from

- `exclude_from_light_attachment_group` (bool): [Read-Write] If set, then it overrides any bLightAttachmentsAsGroup set in a parent.

- `fill_collision_underneath_for_navmesh` (bool): [Read-Write] If set, navmesh will not be generated under the surface of the geometry

- `first_person_primitive_type` (FirstPersonPrimitiveType): [Read-Write] If this is set to FirstPerson, the camera FirstPersonFieldOfView and FirstPersonScale parameters will be used on this component. These parameters can be used to render the component with a different field of view and a smaller depth range such that clipping with the scene can be avoided. This is useful for rendering first person view geometry.

- `force_collision_update` (bool): [Read-Write] Forces the cloth simulation to constantly update its external collisions, at the expense of performance.
This will help to prevent missed collisions if the cloth’s skeletal mesh component isn’t moving,
and when instead, wind or other moving objects are causing new collision shapes to come into the cloth’s vicinity.

- `force_mip_streaming` (bool): [Read-Write] If true, forces mips for textures used by this component to be resident when this component’s level is loaded.

- `forced_lod_model` (int32): [Read-Write]

- `generate_overlap_events` (bool): [Read-Write]

- `global_anim_rate_scale` (float): [Read-Write] Used to scale speed of all animations on this skeletal mesh.

- `has_per_instance_hit_proxies` (bool): [Read-Write] If true a hit-proxy will be generated for each instance of instanced static meshes.
This allows for other systems, like selection in viewports, to function at the individual instance.

- `hidden_in_game` (bool): [Read-Write] Whether to hide the primitive in game, if the primitive is Visible.

- `hidden_in_scene_capture` (bool): [Read-Write] When true, will not be captured by Scene Capture

- `hlod_batching_policy` (HLODBatchingPolicy): [Read-Write] Determines how the geometry of a component will be incorporated in proxy (simplified) HLODs.

- `holdout` (bool): [Read-Write] If this is True, this primitive will render black with an alpha of 0, but all secondary effects (shadows, reflections, indirect lighting) remain. This feature requires activating the project setting(s) “Alpha Output”, and “Support Primitive Alpha Holdout” if using the deferred renderer.

- `ignore_leader_pose_component_lod` (bool): [Read-Write] Flag that when set will ensure UpdateLODStatus will not take the LeaderPoseComponent’s current LOD in consideration when determining the correct LOD level (this requires LeaderPoseComponent’s LOD to always be >= determined LOD otherwise bone transforms could be missing

- `ignore_radial_force` (bool): [Read-Write] Will ignore radial forces applied to this component.

- `ignore_radial_impulse` (bool): [Read-Write] Will ignore radial impulses applied to this component.

- `include_component_location_into_bounds` (bool): [Read-Write] If true, the Location of this Component will be included into its bounds calculation
(this can be useful when using SMU\_OnlyTickPoseWhenRendered on a character that moves away from the root and no bones are left near the origin of the component)

- `indirect_lighting_cache_quality` (IndirectLightingCacheQuality): [Read-Write] Quality of indirect lighting for Movable primitives. This has a large effect on Indirect Lighting Cache update time.

- `is_editor_only` (bool): [Read-Write] If true, the component will be excluded from non-editor builds

- `kinematic_bones_update_type` (KinematicBonesUpdateToPhysics): [Read-Write] If we are running physics, should we update non-simulated bones based on the animation bone positions.

- `ld_max_draw_distance` (float): [Read-Write] Max draw distance exposed to LDs. The real max draw distance is the min (disregarding 0) of this and volumes affecting this object.

- `leader_pose_component` (SkinnedMeshComponent): [Read-Write] If set, this SkeletalMeshComponent will not use its SpaceBase for bone transform, but will
use the component space transforms from the LeaderPoseComponent. This is used when constructing a character using multiple skeletal meshes sharing the same
skeleton within the same Actor.

- `light_attachments_as_group` (bool): [Read-Write] Whether to light this component and any attachments as a group. This only has effect on the root component of an attachment tree.
When enabled, attached component shadowing settings like bCastInsetShadow, bCastVolumetricTranslucentShadow, etc, will be ignored.
This is useful for improving performance when multiple movable components are attached together.

- `lighting_channels` (LightingChannels): [Read-Write] Channels that this component should be in. Lights with matching channels will affect the component.
These channels only apply to opaque materials, direct lighting, and dynamic lighting and shadowing.
Lighting channels are only supported on translucent materials using forward shading (i.e. when not using the translucency lighting volume).

- `lightmap_type` (LightmapType): [Read-Write]

- `material_slots_overlay_material` (Array[MaterialInterface]): [Read-Write] Translucent material to blend on top of this mesh. Mesh will be rendered twice - once with a base material and once with overlay material.
The difference with the global OverlayMaterial is those are per material slot, if the entry is null or doesn’t exist the global
OverlayMaterial will be use for sections using the material slot.

- `mesh_deformer` (MeshDeformer): [Read-Write] The mesh deformer to use. Set to None to disable the deformer on the SkeletalMesh. If no deformer is set from here or the SkeletalMesh, we fall back to the fixed function deformation, unless AlwaysUseMeshDeformer is on.

- `mesh_deformer_instance` (MeshDeformerInstance): [Read-Write]
deprecated: Use the GetMeshDeformerInstance function instead

- `mesh_deformer_instance_settings` (MeshDeformerInstanceSettings): [Read-Only] Object containing instance settings for the bound MeshDeformer.

- `min_draw_distance` (float): [Read-Write] The minimum distance at which the primitive should be rendered,
measured in world space units from the center of the primitive’s bounding sphere to the camera position.

- `min_lod_model` (int32): [Read-Write] This is the min LOD that this component will use. (e.g. if set to 2 then only 2+ LOD Models will be used.) This is useful to set on
meshes which are known to be a certain distance away and still want to have better LODs when zoomed in on them.

- `mobility` (ComponentMobility): [Read-Write] How often this component is allowed to move, used to make various optimizations. Only safe to set in constructor.

- `multi_body_overlap` (bool): [Read-Write] If true, this component will generate individual overlaps for each overlapping physics body if it is a multi-body component. When false, this component will
generate only one overlap, regardless of how many physics bodies it has and how many of them are overlapping another component/body. This flag has no
influence on single body components.

- `nanite_pixel_programmable_distance` (float): [Read-Write] Used to forcefully disable pixel programmable rasterization of Nanite when the mesh is further than a given distance from the camera.

- `never_distance_cull` (bool): [Read-Write] When enabled this object will not be culled by distance. This is ignored if a child of a HLOD.

- `no_skeleton_update` (bool): [Read-Write] Skips Ticking and Bone Refresh.

- `on_anim_initialized` (OnAnimInitialized): [Read-Write] Broadcast when the components anim instance is initialized

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

- `on_constraint_broken` (ConstraintBrokenSignature): [Read-Write] Notification when constraint is broken.

- `on_end_cursor_over` (ComponentEndCursorOverSignature): [Read-Write] Event called when the mouse cursor is moved off this component and mouse over events are enabled in the player controller

- `on_input_touch_begin` (ComponentOnInputTouchBeginSignature): [Read-Write] Event called when a touch input is received over this component when touch events are enabled in the player controller

- `on_input_touch_end` (ComponentOnInputTouchEndSignature): [Read-Write] Event called when a touch input is released over this component when touch events are enabled in the player controller

- `on_input_touch_enter` (ComponentBeginTouchOverSignature): [Read-Write] Event called when a finger is moved over this component when touch over events are enabled in the player controller

- `on_input_touch_leave` (ComponentEndTouchOverSignature): [Read-Write] Event called when a finger is moved off this component when touch over events are enabled in the player controller

- `on_plastic_deformation` (PlasticDeformationEventSignature): [Read-Write] Notification when constraint plasticity drive target changes.

- `on_released` (ComponentOnReleasedSignature): [Read-Write] Event called when the left mouse button is released while the mouse is over this component click events are enabled in the player controller

- `only_owner_see` (bool): [Read-Write] If this is True, this component will only be visible when the view actor is the component’s owner, directly or indirectly.

- `overlay_material` (MaterialInterface): [Read-Write] Translucent material to blend on top of this mesh. Mesh will be rendered twice - once with a base material and once with overlay material

- `overlay_material_max_draw_distance` (float): [Read-Write] The max draw distance for overlay material. A distance of 0 indicates that overlay will be culled using primitive max distance.

- `override_default_animating_rig` (bool): [Read-Write] If true, DefaultAnimatingRigOverride will be used. If false, use the DefaultAnimatingRig in the SkeletalMesh

- `override_materials` (Array[MaterialInterface]): [Read-Write] Material overrides.

- `override_min_lod` (bool): [Read-Write] Whether we should use the min lod specified in MinLodModel for this component instead of the min lod in the mesh

- `owner_no_see` (bool): [Read-Write] If this is True, this component won’t be visible when the view actor is the component’s owner, directly or indirectly. Will be internally set to true when FirstPersonPrimitiveType is set to WorldSpaceRepresentation.

- `pause_anims` (bool): [Read-Write] pauses this component’s animations (doesn’t tick them, but still refreshes bones)

- `per_bone_motion_blur` (bool): [Read-Write] If true, use per-bone motion blur on this skeletal mesh (requires additional rendering, can be disabled to save performance).

- `physics_asset_override` (PhysicsAsset): [Read-Write] PhysicsAsset is set in SkeletalMesh by default, but you can override with this value

- `physics_transform_update_mode` (PhysicsTransformUpdateMode): [Read-Write] Whether physics simulation updates component transform.

- `physics_volume_changed_delegate` (PhysicsVolumeChanged): [Read-Write] Delegate that will be called when PhysicsVolume has been changed \*

- `post_process_anim_bplod_threshold` (int32): [Read-Write] \* Max LOD level that post-process AnimBPs are evaluated. Overrides the setting of the same name on the skeletal mesh.
\\* For example if you have the threshold set to 2, it will evaluate until including LOD 2 (based on 0 index). In case the LOD level gets set to 3, it will stop evaluating the post-process AnimBP.
\\* Setting it to -1 will always evaluate it and disable LODing overrides for this component.

- `primary_component_tick` (ActorComponentTickFunction): [Read-Write] Main tick function for the Component

- `propagate_curves_to_followers` (bool): [Read-Write] If true, propagates calls to ApplyAnimationCurvesToComponent for follower components, only needed if follower components do not tick themselves

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

- `render_static` (bool): [Read-Write] If true, render as static in reference pose.

- `replicate_physics_to_autonomous_proxy` (bool): [Read-Write] True if physics should be replicated to autonomous proxies. This should be true for

server-authoritative simulations, and false for client authoritative simulations.

- `replicate_using_registered_sub_object_list` (bool): [Read-Write] When true the replication system will only replicate the registered subobjects list
When false the replication system will instead call the virtual ReplicateSubObjects() function where the subobjects need to be manually replicated.

- `replicates` (bool): [Read-Write] Is this component currently replicating? Should the network code consider it for replication? Owning Actor must be replicating first!

- `reset_after_teleport` (bool): [Read-Write] reset the clothing after moving the clothing position (called teleport)

- `return_material_on_move` (bool): [Read-Write] If true, component sweeps will return the material in their hit result.
see: MoveComponent(), FHitResult

- `runtime_virtual_textures` (Array[RuntimeVirtualTexture]): [Read-Write] Array of runtime virtual textures into which we draw the mesh for this actor.
The material also needs to be set up to output to a virtual texture.

- `self_shadow_only` (bool): [Read-Write] When enabled, the component will only cast a shadow on itself and not other components in the world.
This is especially useful for first person weapons, and forces bCastInsetShadow to be enabled.

- `set_mesh_deformer` (bool): [Read-Write] If true, MeshDeformer will be used. If false, use the default mesh deformer on the SkeletalMesh.

- `shadow_cache_invalidation_behavior` (ShadowCacheInvalidationBehavior): [Read-Write] Control shadow invalidation behavior, in particular with respect to Virtual Shadow Maps and material effects like World Position Offset.

- `should_update_physics_volume` (bool): [Read-Write] Whether or not the cached PhysicsVolume this component overlaps should be updated when the component is moved.
see: GetPhysicsVolume()

- `single_sample_shadow_from_stationary_lights` (bool): [Read-Write] Whether the whole component should be shadowed as one from stationary lights, which makes shadow receiving much cheaper.
When enabled shadowing data comes from the volume lighting samples precomputed by Lightmass, which are very sparse.
This is currently only used on stationary directional lights.

- `skeletal_mesh` (SkeletalMesh): [Read-Write]
deprecated: Use USkeletalMeshComponent::GetSkeletalMeshAsset() or GetSkinnedAsset() instead.

- `skeletal_mesh_asset` (SkeletalMesh): [Read-Write]

- `skin_cache_usage` (Array[SkinCacheUsage]): [Read-Write] How this Component’s LOD uses the skin cache feature. Auto will defer to the asset’s (SkeletalMesh) option. If Ray Tracing is enabled, will imply Enabled

- `skinned_asset` (SkinnedAsset): [Read-Write]

- `skip_bounds_update_when_interpolating` (bool): [Read-Write] Whether to skip bounds update when interpolating. Bounds are updated to the target interpolation pose only on ticks when they are evaluated.

- `skip_kinematic_update_when_interpolating` (bool): [Read-Write] Whether to skip UpdateKinematicBonesToAnim() when interpolating. Kinematic bones are updated to the target interpolation pose only on ticks when they are evaluated.

- `sort_triangles` (bool): [Read-Write] Enable dynamic sort mesh’s triangles to remove ordering issue when rendered with a translucent material

- `static_when_not_moveable` (bool): [Read-Write] When false, the underlying physics body will contain all sim data (mass, inertia tensor, etc) even if mobility is not set to Moveable

- `streaming_distance_multiplier` (float): [Read-Write] Allows adjusting the desired streaming distance of streaming textures that uses UV 0.
1.0 is the default, whereas a higher value makes the textures stream in sooner from far away.
A lower value (0.0-1.0) makes the textures stream in later (you have to be closer).
Value can be < 0 (from legcay content, or code changes)

- `sync_attach_parent_lod` (bool): [Read-Write] If true, this component uses its parents LOD when attached if available
ForcedLOD can override this change. By default, it will use parent LOD.

- `teleport_distance_threshold` (float): [Read-Write] Conduct teleportation if the character’s movement is greater than this threshold in 1 frame.
Zero or negative values will skip the check.
You can also do force teleport manually using ForceNextUpdateTeleport() / ForceNextUpdateTeleportAndReset().

- `teleport_rotation_threshold` (float): [Read-Write] Rotation threshold in degrees, ranging from 0 to 180.
Conduct teleportation if the character’s rotation is greater than this threshold in 1 frame.
Zero or negative values will skip the check.

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

- `update_animation_in_editor` (bool): [Read-Write] If true, this will Tick until disabled

- `update_cloth_in_editor` (bool): [Read-Write] If true, will play cloth in editor

- `update_joints_from_animation` (bool): [Read-Write] If we should pass joint position to joints each frame, so that they can be used by motorized joints to drive the
ragdoll based on the animation.

- `update_mesh_when_kinematic` (bool): [Read-Write] If true, then the physics bodies will be used to drive the skeletal mesh even when they are
kinematic (not simulating), otherwise the skeletal mesh will be driven by the animation input
when the bodies are kinematic

- `update_overlaps_on_animation_finalize` (bool): [Read-Write] Controls whether blending in physics bones will refresh overlaps on this component, defaults to true but can be disabled in cases where we know anim->physics blending doesn’t meaningfully change overlaps

- `use_as_occluder` (bool): [Read-Write] Whether to render the primitive in the depth only pass.
This should generally be true for all objects, and let the renderer make decisions about whether to render objects in the depth only pass.
todo: if any rendering features rely on a complete depth only pass, this variable needs to go away.

- `use_attach_parent_bound` (bool): [Read-Write] If true, this component uses its parents bounds when attached.
This can be a significant optimization with many components attached together.

- `use_bounds_from_leader_pose_component` (bool): [Read-Write] When true, we will just using the bounds from our LeaderPoseComponent. This is useful for when we have a Mesh Parented
to the main SkelMesh (e.g. outline mesh or a full body overdraw effect that is toggled) that is always going to be the same
bounds as parent. We want to do no calculations in that case.

- `use_ref_pose_on_init_anim` (bool): [Read-Write] On InitAnim should we set to ref pose (if false use first tick of animation data). If enabled, takes precedence over UAnimationSettings::bTickAnimationOnSkeletalMeshInit

- `use_screen_render_state_for_update` (bool): [Read-Write] If set, use the screen render flag instead of the default render flag when processing offscreen-rendering optimizations
(such as VisibilityBasedAnimTickOption) that look to reduce animation work when the mesh is not rendered.
Using this option can result in meshes that are occlusion culled ceasing to perform animation work.
Note that this can however result in shadows not being animated when meshes are not directly visible.

- `virtual_texture_cull_mips` (int8): [Read-Write] Number of lower mips in the runtime virtual texture to skip for rendering this primitive.
Larger values reduce the effective draw distance in the runtime virtual texture.
This culling method doesn’t take into account primitive size or virtual texture size.

- `virtual_texture_lod_bias` (int8): [Read-Write] Bias to the LOD selected for rendering to runtime virtual textures.

- `virtual_texture_min_coverage` (int8): [Read-Write] Set the minimum pixel coverage before culling from the runtime virtual texture.
Larger values reduce the effective draw distance in the runtime virtual texture.

- `virtual_texture_render_pass_type` (RuntimeVirtualTextureMainPassType): [Read-Write] Controls if this component draws in the main pass as well as in the virtual texture.

- `visibility_based_anim_tick_option` (VisibilityBasedAnimTickOption): [Read-Write] \* This is tick animation frequency option based on this component rendered or not or using montage
\\* You can change this default value in the INI file
\\* Mostly related with performance

- `visible` (bool): [Read-Write] Whether to completely draw the primitive; if false, the primitive is not drawn, does not cast a shadow.

- `visible_in_ray_tracing` (bool): [Read-Write] If true, this component will be visible in ray tracing effects. Turning this off will remove it from ray traced reflections, shadows, etc.

- `visible_in_real_time_sky_captures` (bool): [Read-Write] If true, this component will be visible in real-time sky light reflection captures.

- `visible_in_reflection_captures` (bool): [Read-Write] If true, this component will be visible in reflection captures.

- `visible_in_scene_capture_only` (bool): [Read-Write] When true, will only be visible in Scene Capture

- `wait_for_parallel_cloth_task` (bool): [Read-Write] Whether we should stall the Cloth tick task until the cloth simulation is complete. This is required if we want up-to-date
cloth data on the game thread, for example if we want to generate particles at cloth vertices.



---

**accumulate_all_bodies_below_physics_blend_weight**( _bone_name_, _add_physics_blend_weight_, _skip_custom_physics_type=False_) → `None`

Accumulate AddPhysicsBlendWeight to physics blendweight for all of the bones below passed in bone to be simulated

Parameters:

- **bone\_name** ( _Name_)

- **add\_physics\_blend\_weight** ( _float_)

- **skip\_custom\_physics\_type** ( _bool_)



---

**add_cloth_collision_source**( _source_component_, _source_physics_asset_) → `None`

Add a collision source for the cloth on this component.
Each cloth tick, the collision defined by the physics asset, transformed by the bones in the source
component, will be applied to cloth.

Parameters:

- **source\_component** ( _SkeletalMeshComponent_) – The component to extract collision transforms from

- **source\_physics\_asset** ( _PhysicsAsset_) – The physics asset that defines the collision primitives (that will be transformed by InSourceComponent’s bones)



---

**add_force_to_all_bodies_below**( _force_, _bone_name='None'_, _accel_change=False_, _include_self=True_) → `None`

Add a force to all rigid bodies below.
This is like a ‘thruster’. Good for adding a burst over some (non zero) time. Should be called every frame for the duration of the force.

Parameters:

- **force** ( _Vector_) – Force vector to apply. Magnitude indicates strength of force.

- **bone\_name** ( _Name_) – If a SkeletalMeshComponent, name of body to apply force to. ‘None’ indicates root body.

- **accel\_change** ( _bool_) – If true, Force is taken as a change in acceleration instead of a physical force (i.e. mass will have no effect).

- **include\_self** ( _bool_) – If false, Force is only applied to bodies below but not given bone name.



---

**add_impulse_to_all_bodies_below**( _impulse_, _bone_name='None'_, _vel_change=False_, _include_self=True_) → `None`

Add impulse to all single rigid bodies below. Good for one time instant burst.

Parameters:

- **impulse** ( _Vector_) – Magnitude and direction of impulse to apply.

- **bone\_name** ( _Name_) – If a SkeletalMeshComponent, name of body to apply impulse to. ‘None’ indicates root body.

- **vel\_change** ( _bool_) – If true, the Strength is taken as a change in velocity instead of an impulse (ie. mass will have no effect).

- **include\_self** ( _bool_) – If false, Force is only applied to bodies below but not given bone name.



---

**allow_anim_curve_evaluation**( _name_of_curve_, _allow_) → `None`

Allow Anim Curve Evaluation

Parameters:

- **name\_of\_curve** ( _Name_)

- **allow** ( _bool_)



---

_property_ `allow_cloth_actors`: bool

[Read-Write] Toggles creation of cloth simulation. Distinct from the simulation toggle below in that, if off, avoids allocating
the actors entirely instead of just skipping the simulation step.

**Type:**

( bool)


---

_property_ `anim_blueprint_generated_class`: AnimBlueprintGeneratedClass

[Read-Only]

**Type:**

( type( AnimBlueprintGeneratedClass))


---

_property_ `anim_class`: Class

[Read-Only] The AnimBlueprint class to use. Use ‘SetAnimInstanceClass’ to change at runtime.

**Type:**

( type( Class))


---

_property_ `animation_blueprint`: AnimBlueprintGeneratedClass

‘animation\_blueprint’ was renamed to ‘anim\_blueprint\_generated\_class’.

**Type:**

deprecated


---

_property_ `animation_data`: SingleAnimationPlayData

[Read-Write]

**Type:**

( SingleAnimationPlayData)


---

_property_ `animation_mode`: AnimationMode

[Read-Only] Whether to use Animation Blueprint or play Single Animation Asset.

**Type:**

( AnimationMode)


---

_property_ `b_propagate_curves_to_slaves`: bool

‘b\_propagate\_curves\_to\_slaves’ was renamed to ‘propagate\_curves\_to\_followers’.

**Type:**

deprecated


---

**bind_cloth_to_leader_pose_component**() → `None`

If this component has a valid LeaderPoseComponent then this function makes cloth items on the follower component
take the transforms of the cloth items on the leader component instead of simulating separately.
Note: This will FORCE any cloth actor on the leader component to simulate in local space. Also The meshes used in the components must be identical for the cloth to bind correctly


---

**bind_cloth_to_master_pose_component**() → `None`

deprecated: ‘bind\_cloth\_to\_master\_pose\_component’ was renamed to ‘bind\_cloth\_to\_leader\_pose\_component’.


---

**break_constraint**( _impulse_, _hit_location_, _bone_name_) → `None`

Break a constraint off a Gore mesh.

Parameters:

- **impulse** ( _Vector_) – vector of impulse

- **hit\_location** ( _Vector_) – location of the hit

- **bone\_name** ( _Name_) – Name of bone to break constraint for



---

**clear_layer_overlay**( _class_:Class_) → `None`

deprecated: ‘clear\_layer\_overlay’ was renamed to ‘unlink\_anim\_class\_layers’.


---

**clear_morph_targets**() → `None`

Clear all Morph Target that are set to this mesh


---

_property_ `cloth_blend_weight`: float

[Read-Write] weight to blend between simulated results and key-framed positions
if weight is 1.0, shows only cloth simulation results and 0.0 will show only skinned results

**Type:**

( float)


---

_property_ `cloth_geometry_scale`: float

[Read-Write] This scale is applied to all cloth geometry (e.g., cloth meshes and collisions) in order to simulate in a different scale space than world.This scale is not applied to distance-based simulation parameters such as MaxDistance.
This property is currently only read by the cloth solver when creating cloth actors, but may become animatable in the future.

**Type:**

( float)


---

_property_ `cloth_max_distance_scale`: float

[Read-Write]

**Type:**

( float)


---

_property_ `cloth_teleport_mode`: ClothingTeleportMode

[Read-Only] whether we need to teleport cloth. // This property is explicitly hidden from the details panel inside FSkeletalMeshComponentDetails::UpdatePhysicsCategory

**Type:**

( ClothingTeleportMode)


---

_property_ `cloth_velocity_scale`: float

[Read-Write] Scale applied to the component induced velocity of all cloth particles prior to stepping the cloth solver.
Use 1.0 for fully induced velocity (default), or use 0.0 for no induced velocity, and any other values in between for a reduced induced velocity.
When set to 0.0, it also provides a way to force the clothing to simulate in local space.
This value multiplies to individual cloth’s velocity scale settings, still allowing for differences in behavior between the various pieces of clothing within the same component.

**Type:**

( float)


---

_property_ `collide_with_attached_children`: bool

[Read-Write] can’t collide with part of attached children if total collision volumes exceed 16 capsules or 32 planes per convex

**Type:**

( bool)


---

_property_ `collide_with_environment`: bool

[Read-Write] can’t collide with part of environment if total collision volumes exceed 16 capsules or 32 planes per convex

**Type:**

( bool)


---

_property_ `default_animating_rig_override`: Object

[Read-Write] Default Animating Rig to Use if bOverrideDefaultAnimatingRig is true

**Type:**

( Object)


---

_property_ `defer_kinematic_bone_update`: bool

[Read-Only] Whether animation and world transform updates are deferred. If this is on, the kinematic bodies (scene query data) will not update until the next time the physics simulation is run

**Type:**

( bool)


---

_property_ `disable_cloth_simulation`: bool

[Read-Write] Disable cloth simulation and play original animation without simulation

**Type:**

( bool)


---

_property_ `disable_post_process_blueprint`: bool

[Read-Write] Controls whether or not this component will evaluate its post process instance. The post-process
Instance is dictated by the skeletal mesh so this is used for per-instance control.

**Type:**

( bool)


---

_property_ `enable_animation`: bool

[Read-Only] Whether the built-in animation of this component should run when the component ticks.
It is assumed that if this is false then some external system will be animating this mesh.
Note that disabling animation will also cause cloth simulation not to run and the component’s tick to run on any thread.

**Type:**

( bool)


---

_property_ `enable_per_poly_collision`: bool

[Read-Only] Uses skinned data for collision data.

**Type:**

( bool)


---

_property_ `enable_physics_on_dedicated_server`: bool

[Read-Write] If true, simulate physics for this component on a dedicated server.
This should be set if simulating physics and replicating with a dedicated server.

> Note: This property cannot be changed at runtime.

**Type:**

( bool)


---

**find_constraint_bone_name**( _constraint_index_) → `Name`

Find Constraint Name from index

Parameters:

**constraint\_index** ( _int32_) – Index of constraint to look for

Returns:

Constraint Joint Name

Return type:

Name


---

**force_cloth_next_update_teleport**() → `None`

Used to indicate we should force ‘teleport’ during the next call to UpdateClothState,
This will transform positions and velocities and thus keep the simulation state, just translate it to a new pose.


---

**force_cloth_next_update_teleport_and_reset**() → `None`

Used to indicate we should force ‘teleport and reset’ during the next call to UpdateClothState.
This can be used to reset it from a bad state or by a teleport where the old state is not important anymore.


---

_property_ `force_collision_update`: bool

[Read-Write] Forces the cloth simulation to constantly update its external collisions, at the expense of performance.
This will help to prevent missed collisions if the cloth’s skeletal mesh component isn’t moving,
and when instead, wind or other moving objects are causing new collision shapes to come into the cloth’s vicinity.

**Type:**

( bool)


---

**get_allow_cloth_actors**() → `bool`

Get Allow Cloth Actors

Return type:

bool


---

**get_allow_rigid_body_anim_node**() → `bool`

Get Allow Rigid Body Anim Node

Return type:

bool


---

**get_allowed_anim_curve_evaluate**() → `bool`

Get Allowed Anim Curve Evaluate

Return type:

bool


---

**get_anim_instance**() → `AnimInstance`

Returns the animation instance that is driving the class (if available). This is typically an instance of
the class set as AnimBlueprintGeneratedClass (generated by an animation blueprint)
Since this instance is transient, it is not safe to be used during construction script

Return type:

AnimInstance


---

**get_animation_mode**() → `AnimationMode`

Get Animation Mode

Return type:

AnimationMode


---

**get_bone_linear_velocity**( _bone_name_) → `Vector`

Get Bone Linear Velocity

Parameters:

**bone\_name** ( _Name_)

Return type:

Vector


---

**get_bone_mass**( _bone_name='None'_, _scale_mass=True_) → `float`

Returns the mass (in kg) of the given bone

Parameters:

- **bone\_name** ( _Name_) – Name of the body to return. ‘None’ indicates root body.

- **scale\_mass** ( _bool_) – If true, the mass is scaled by the bone’s MassScale.


Return type:

float


---

**get_closest_point_on_physics_asset**( _world_position_) → `(closest_world_position=Vector,normal=Vector,bone_name=Name,distance=float)orNone`

Given a world position, find the closest point on the physics asset. Note that this is independent of collision and welding. This is based purely on animation position

Parameters:

**world\_position** ( _Vector_) – The point we want the closest point to (i.e. for all bodies in the physics asset, find the one that has a point closest to WorldPosition)

Returns:

true if we found a closest point

closest\_world\_position (Vector):

normal (Vector):

bone\_name (Name):

distance (float):

Return type:

tuple or None


---

**get_cloth_max_distance_scale**() → `float`

Get/Set the max distance scale of clothing mesh vertices

Return type:

float


---

**get_clothing_simulation_interactor**( _clothing_asset_name='None'_) → `ClothingSimulationInteractor`

Get the interactor for a clothing simulation, if that simulation supports runtime interaction.
note: Using NAME\_None when there are clothing data of different types on the Skeletal Mesh asset will cause a warning.

Parameters:

**clothing\_asset\_name** ( _Name_)

Return type:

ClothingSimulationInteractor


---

**get_constraint_by_name**( _constraint_name_, _includes_terminated_) → `ConstraintInstanceAccessor`

Gets a constraint by its name

Parameters:

- **constraint\_name** ( _Name_) – name of the constraint

- **includes\_terminated** ( _bool_)


Return type:

ConstraintInstanceAccessor


---

**get_constraints**( _includes_terminated_) → `Array\ [ConstraintInstanceAccessor]`

Gets all the constraints

Parameters:

**includes\_terminated** ( _bool_)

Returns:

out\_constraints (Array[ConstraintInstanceAccessor]): returned list of constraints matching the parameters

Return type:

Array\ [ConstraintInstanceAccessor]


---

**get_constraints_from_body**( _body_name_, _parent_constraints_, _child_constraints_, _includes_terminated_) → `Array\ [ConstraintInstanceAccessor]`

Gets all the constraints attached to a body

Parameters:

- **body\_name** ( _Name_) – name of the body to get the attached constraints from

- **parent\_constraints** ( _bool_) – return constraints where BodyName is the child of the constraint

- **child\_constraints** ( _bool_) – return constraints where BodyName is the parent of the constraint

- **includes\_terminated** ( _bool_)


Returns:

out\_constraints (Array[ConstraintInstanceAccessor]): returned list of constraints matching the parameters

Return type:

Array\ [ConstraintInstanceAccessor]

get\_current\_joint\_angles( _bone\_name)->(swing1\_angle=float_, _twist\_angle=float_, _swing2\_angle=float_)

Gets the current Angular state for a named bone constraint

Parameters:

**bone\_name** ( _Name_) – Name of bone to get constraint ranges for

Returns:

swing1\_angle (float): current angular state of the constraint

twist\_angle (float): current angular state of the constraint

swing2\_angle (float): current angular state of the constraint

Return type:

tuple


---

**get_curve_value**( _curve_name_, _default_value_) → `floatorNone`

Get curve value

Parameters:

- **curve\_name** ( _Name_) – Name of the curve to retrieve

- **default\_value** ( _float_) – In case the curve could not be found


Returns:

Whether the curve was successfully retrieved

value (float): Retrieved curve value if found, otherwise is set to DefaultValue

Return type:

float or None


---

**get_default_animating_rig**() → `Object`

Get Default Animating Rig

Return type:

Object


---

**get_disable_anim_curves**() → `bool`

Get Disable Anim Curves

Return type:

bool


---

**get_float_attribute**( _bone_name_, _attribute_name_, _default_value_, _lookup_type=CustomBoneAttributeLookup.BONE_ONLY_) → `floatorNone`

Get float type attribute value.

Parameters:

- **bone\_name** ( _Name_) – Name of the bone to retrieve try and retrieve the attribute from

- **attribute\_name** ( _Name_) – Name of the attribute to retrieve

- **default\_value** ( _float_) – In case the attribute could not be found

- **lookup\_type** ( _CustomBoneAttributeLookup_) – Determines how the attribute is retrieved from the specified BoneName (see ECustomBoneAttributeLookup)


Returns:

Whether or not the atttribute was successfully retrieved

out\_value (float): Retrieved attribute value if found, otherwise is set to DefaultValue

Return type:

float or None


---

**get_float_attribute_ref**( _bone_name_, _attribute_name_, _out_value_, _lookup_type=CustomBoneAttributeLookup.BONE_ONLY_) → `floatorNone`

Get float type attribute value.

Parameters:

- **bone\_name** ( _Name_) – Name of the bone to retrieve try and retrieve the attribute from

- **attribute\_name** ( _Name_) – Name of the attribute to retrieve

- **out\_value** ( _float_) – (reference) Retrieved attribute value if found, otherwise is set to DefaultValue

- **lookup\_type** ( _CustomBoneAttributeLookup_) – Determines how the attribute is retrieved from the specified BoneName (see ECustomBoneAttributeLookup)


Returns:

Whether or not the atttribute was successfully retrieved

out\_value (float): (reference) Retrieved attribute value if found, otherwise is set to DefaultValue

Return type:

float or None


---

**get_integer_attribute**( _bone_name_, _attribute_name_, _default_value_, _lookup_type=CustomBoneAttributeLookup.BONE_ONLY_) → `int32orNone`

Get integer type attribute value.

Parameters:

- **bone\_name** ( _Name_) – Name of the bone to retrieve try and retrieve the attribute from

- **attribute\_name** ( _Name_) – Name of the attribute to retrieve

- **default\_value** ( _int32_) – In case the attribute could not be found

- **lookup\_type** ( _CustomBoneAttributeLookup_) – Determines how the attribute is retrieved from the specified BoneName (see ECustomBoneAttributeLookup)


Returns:

Whether or not the atttribute was successfully retrieved

out\_value (int32): Retrieved attribute value if found, otherwise is set to DefaultValue

Return type:

int32 or None


---

**get_integer_attribute_ref**( _bone_name_, _attribute_name_, _out_value_, _lookup_type=CustomBoneAttributeLookup.BONE_ONLY_) → `int32orNone`

Get integer type attribute value.

Parameters:

- **bone\_name** ( _Name_) – Name of the bone to retrieve try and retrieve the attribute from

- **attribute\_name** ( _Name_) – Name of the attribute to retrieve

- **out\_value** ( _int32_) – (reference) Retrieved attribute value if found, otherwise is set to DefaultValue

- **lookup\_type** ( _CustomBoneAttributeLookup_) – Determines how the attribute is retrieved from the specified BoneName (see ECustomBoneAttributeLookup)


Returns:

Whether or not the atttribute was successfully retrieved

out\_value (int32): (reference) Retrieved attribute value if found, otherwise is set to DefaultValue

Return type:

int32 or None


---

**get_layer_sub_instance_by_class**( _class_:Class_) → `AnimInstance`

deprecated: ‘get\_layer\_sub\_instance\_by\_class’ was renamed to ‘get\_linked\_anim\_layer\_instance\_by\_class’.


---

**get_layer_sub_instance_by_group**( _group:Name_) → `AnimInstance`

deprecated: ‘get\_layer\_sub\_instance\_by\_group’ was renamed to ‘get\_linked\_anim\_layer\_instance\_by\_group’.


---

**get_linked_anim_graph_instance_by_tag**( _tag_) → `AnimInstance`

Returns the a tagged linked instance node. If no linked instances are found or none are tagged with the
supplied name, this will return NULL.

Parameters:

**tag** ( _Name_)

Return type:

AnimInstance


---

**get_linked_anim_graph_instances_by_tag**( _tag_) → `Array\ [AnimInstance]`

Get Linked Anim Graph Instances by Tag
deprecated: Tags are unique so this function is no longer supported. Please use GetLinkedAnimGraphInstanceByTag instead

Parameters:

**tag** ( _Name_)

Returns:

out\_linked\_instances (Array[AnimInstance]):

Return type:

Array\ [AnimInstance]


---

**get_linked_anim_layer_instance_by_class**( _class__) → `AnimInstance`

Gets the first layer linked instance corresponding to the specified class

Parameters:

**class** ( _type_ _(_ _Class_ _)_)

Return type:

AnimInstance


---

**get_linked_anim_layer_instance_by_group**( _group_) → `AnimInstance`

Gets the layer linked instance corresponding to the specified group

Parameters:

**group** ( _Name_)

Return type:

AnimInstance


---

**get_morph_target**( _morph_target_name_) → `float`

Get Morph target with given name

Parameters:

**morph\_target\_name** ( _Name_)

Return type:

float


---

**get_play_rate**() → `floatAnimation play functions`

- These changes status of animation instance, which is transient data, which means it won’t serialize with this component

- Because of that reason, it is not safe to be used during construction script

- Please use OverrideAnimationData for construction script. That will override AnimationData to be serialized


Return type:

float


---

**get_position**() → `floatAnimation play functions`

- These changes status of animation instance, which is transient data, which means it won’t serialize with this component

- Because of that reason, it is not safe to be used during construction script

- Please use OverrideAnimationData for construction script. That will override AnimationData to be serialized


Return type:

float


---

**get_post_process_instance**() → `AnimInstance`

Returns the active post process instance is one is available. This is set on the mesh that this
component is using, and is evaluated immediately after the main instance.

Return type:

AnimInstance


---

**get_skeletal_center_of_mass**() → `Vector`

Returns the center of mass of the skeletal mesh, instead of the root body’s location

Return type:

Vector


---

**get_skeletal_mesh_asset**() → `SkeletalMesh`

Get the SkeletalMesh rendered for this mesh.

Return type:

SkeletalMesh


---

**get_string_attribute**( _bone_name_, _attribute_name_, _default_value_, _lookup_type=CustomBoneAttributeLookup.BONE_ONLY_) → `strorNone`

Get string type attribute value.

Parameters:

- **bone\_name** ( _Name_) – Name of the bone to retrieve try and retrieve the attribute from

- **attribute\_name** ( _Name_) – Name of the attribute to retrieve

- **default\_value** ( _str_) – In case the attribute could not be found

- **lookup\_type** ( _CustomBoneAttributeLookup_) – Determines how the attribute is retrieved from the specified BoneName (see ECustomBoneAttributeLookup)


Returns:

Whether or not the atttribute was successfully retrieved

out\_value (str): Retrieved attribute value if found, otherwise is set to DefaultValue

Return type:

str or None


---

**get_string_attribute_ref**( _bone_name_, _attribute_name_, _out_value_, _lookup_type=CustomBoneAttributeLookup.BONE_ONLY_) → `strorNone`

Get string type attribute value.

Parameters:

- **bone\_name** ( _Name_) – Name of the bone to retrieve try and retrieve the attribute from

- **attribute\_name** ( _Name_) – Name of the attribute to retrieve

- **out\_value** ( _str_) – (reference) Retrieved attribute value if found, otherwise is set to DefaultValue

- **lookup\_type** ( _CustomBoneAttributeLookup_) – Determines how the attribute is retrieved from the specified BoneName (see ECustomBoneAttributeLookup)


Returns:

Whether or not the atttribute was successfully retrieved

out\_value (str): (reference) Retrieved attribute value if found, otherwise is set to DefaultValue

Return type:

str or None


---

**get_sub_instance_by_tag**( _tag:Name_) → `AnimInstance`

deprecated: ‘get\_sub\_instance\_by\_tag’ was renamed to ‘get\_linked\_anim\_graph\_instance\_by\_tag’.


---

**get_sub_instances_by_tag**( _tag:Name_) → `None`

deprecated: ‘get\_sub\_instances\_by\_tag’ was renamed to ‘get\_linked\_anim\_graph\_instances\_by\_tag’.


---

**get_transform_attribute**( _bone_name_, _attribute_name_, _default_value_, _lookup_type=CustomBoneAttributeLookup.BONE_ONLY_) → `TransformorNone`

Get FTransform type attribute value.

Parameters:

- **bone\_name** ( _Name_) – Name of the bone to retrieve try and retrieve the attribute from

- **attribute\_name** ( _Name_) – Name of the attribute to retrieve

- **default\_value** ( _Transform_)

- **lookup\_type** ( _CustomBoneAttributeLookup_) – Determines how the attribute is retrieved from the specified BoneName (see ECustomBoneAttributeLookup)


Returns:

Whether or not the atttribute was successfully retrieved

out\_value (Transform): (reference) Retrieved attribute value if found, otherwise is set to DefaultValue

Return type:

Transform or None


---

**get_transform_attribute_ref**( _bone_name_, _attribute_name_, _out_value_, _lookup_type=CustomBoneAttributeLookup.BONE_ONLY_) → `TransformorNone`

Get FTransform type attribute value.

Parameters:

- **bone\_name** ( _Name_) – Name of the bone to retrieve try and retrieve the attribute from

- **attribute\_name** ( _Name_) – Name of the attribute to retrieve

- **out\_value** ( _Transform_) – (reference) Retrieved attribute value if found, otherwise is set to DefaultValue

- **lookup\_type** ( _CustomBoneAttributeLookup_) – Determines how the attribute is retrieved from the specified BoneName (see ECustomBoneAttributeLookup)


Returns:

Whether or not the atttribute was successfully retrieved

out\_value (Transform): (reference) Retrieved attribute value if found, otherwise is set to DefaultValue

Return type:

Transform or None


---

_property_ `global_anim_rate_scale`: float

[Read-Write] Used to scale speed of all animations on this skeletal mesh.

**Type:**

( float)


---

**has_valid_animation_instance**() → `bool`

Returns whether there are any valid instances to run, currently this means whether we have
have an animation instance or a post process instance available to process.

Return type:

bool


---

**is_body_gravity_enabled**( _bone_name_) → `bool`

Checks whether or not gravity is enabled on the given bone.
NAME\_None indicates the root body should be queried.
If the bone name given is otherwise invalid, false is returned.

Parameters:

**bone\_name** ( _Name_) – The name of the bone to check.

Returns:

True if gravity is enabled on the bone.

Return type:

bool


---

**is_clothing_simulation_suspended**() → `bool`

Gets whether or not the clothing simulation is currently suspended

Return type:

bool


---

**is_playing**() → `boolAnimation play functions`

- These changes status of animation instance, which is transient data, which means it won’t serialize with this component

- Because of that reason, it is not safe to be used during construction script

- Please use OverrideAnimationData for construction script. That will override AnimationData to be serialized


Return type:

bool


---

**k2_set_anim_instance_class**( _new_class:Class_) → `None`

deprecated: ‘k2\_set\_anim\_instance\_class’ was renamed to ‘set\_anim\_instance\_class’.


---

_property_ `kinematic_bones_update_type`: KinematicBonesUpdateToPhysics

[Read-Write] If we are running physics, should we update non-simulated bones based on the animation bone positions.

**Type:**

( KinematicBonesUpdateToPhysics)


---

**link_anim_class_layers**( _class__) → `None`

Runs through all layer nodes, attempting to find layer nodes that are implemented by the specified class, then sets up a linked instance of the class for each.
Allocates one linked instance to run each of the groups specified in the class, so state is shared. If a layer is not grouped (ie. NAME\_None), then state is not shared
and a separate linked instance is allocated for each layer node.
If InClass is null, then all layers are reset to their defaults.

Parameters:

**class** ( _type_ _(_ _Class_ _)_)


---

**link_anim_graph_by_tag**( _tag_, _class__) → `None`

Runs through all nodes, attempting to find linked instance by name/tag, then sets the class of each node if the tag matches

Parameters:

- **tag** ( _Name_)

- **class** ( _type_ _(_ _Class_ _)_)



---

_property_ `no_skeleton_update`: bool

[Read-Write] Skips Ticking and Bone Refresh.

**Type:**

( bool)


---

_property_ `on_anim_initialized`: OnAnimInitialized

[Read-Write] Broadcast when the components anim instance is initialized

**Type:**

( OnAnimInitialized)


---

_property_ `on_constraint_broken`: ConstraintBrokenSignature

[Read-Write] Notification when constraint is broken.

**Type:**

( ConstraintBrokenSignature)


---

_property_ `on_plastic_deformation`: PlasticDeformationEventSignature

[Read-Write] Notification when constraint plasticity drive target changes.

**Type:**

( PlasticDeformationEventSignature)


---

**override_animation_data**( _anim_to_play_, _is_looping=True_, _is_playing=True_, _position=0.000000_, _play_rate=1.000000_) → `None`

This overrides current AnimationData parameter in the SkeletalMeshComponent. This will serialize when the component serialize
so it can be used during construction script. However note that this will override current existing data
This can be useful if you’d like to make a blueprint with custom default animation per component
This sets single player mode, which means you can’t use AnimBlueprint with it

Parameters:

- **anim\_to\_play** ( _AnimationAsset_)

- **is\_looping** ( _bool_)

- **is\_playing** ( _bool_)

- **position** ( _float_)

- **play\_rate** ( _float_)



---

_property_ `pause_anims`: bool

[Read-Write] pauses this component’s animations (doesn’t tick them, but still refreshes bones)

**Type:**

( bool)


---

_property_ `physics_transform_update_mode`: PhysicsTransformUpdateMode

[Read-Write] Whether physics simulation updates component transform.

**Type:**

( PhysicsTransformUpdateMode)


---

**play**( _looping_) → `NoneAnimation play functions`

- These changes status of animation instance, which is transient data, which means it won’t serialize with this component

- Because of that reason, it is not safe to be used during construction script

- Please use OverrideAnimationData for construction script. That will override AnimationData to be serialized


Parameters:

**looping** ( _bool_)


---

**play_animation**( _new_anim_to_play_, _looping_) → `NoneAnimation play functions`

- These changes status of animation instance, which is transient data, which means it won’t serialize with this component

- Because of that reason, it is not safe to be used during construction script

- Please use OverrideAnimationData for construction script. That will override AnimationData to be serialized


Parameters:

- **new\_anim\_to\_play** ( _AnimationAsset_)

- **looping** ( _bool_)



---

_property_ `post_process_anim_bplod_threshold`: int

[Read-Write] \* Max LOD level that post-process AnimBPs are evaluated. Overrides the setting of the same name on the skeletal mesh.
\\* For example if you have the threshold set to 2, it will evaluate until including LOD 2 (based on 0 index). In case the LOD level gets set to 3, it will stop evaluating the post-process AnimBP.
\\* Setting it to -1 will always evaluate it and disable LODing overrides for this component.

**Type:**

(int32)


---

_property_ `propagate_curves_to_followers`: bool

[Read-Write] If true, propagates calls to ApplyAnimationCurvesToComponent for follower components, only needed if follower components do not tick themselves

**Type:**

( bool)


---

**recreate_clothing_actors**() → `None`

Destroys and recreates the clothing actors in the current simulation


---

**remove_cloth_collision_source**( _source_component_, _source_physics_asset_) → `None`

Remove a cloth collision source defined by both a component and a physics asset

Parameters:

- **source\_component** ( _SkeletalMeshComponent_)

- **source\_physics\_asset** ( _PhysicsAsset_)



---

**remove_cloth_collision_sources**( _source_component_) → `None`

Remove a cloth collision source defined by a component

Parameters:

**source\_component** ( _SkeletalMeshComponent_)


---

_property_ `reset_after_teleport`: bool

[Read-Write] reset the clothing after moving the clothing position (called teleport)

**Type:**

( bool)


---

**reset_all_bodies_simulate_physics**() → `None`

Allows you to reset bodies Simulate state based on where bUsePhysics is set to true in the BodySetup.


---

**reset_allowed_anim_curve_evaluation**() → `None`

By reset, it will allow all the curves to be evaluated


---

**reset_anim_instance_dynamics**( _teleport_type=TeleportType.RESET_PHYSICS_) → `None`

Informs any active anim instances (main instance, linked instances, post instance) that a dynamics reset is required
for example if a teleport occurs.

Parameters:

**teleport\_type** ( _TeleportType_)


---

**reset_cloth_collision_sources**() → `None`

Remove all cloth collision sources


---

**reset_cloth_teleport_mode**() → `None`

Reset the teleport mode of a next update to ‘Continuous’


---

**resume_clothing_simulation**() → `None`

Resumes a previously suspended clothing simulation, teleporting the clothing on the next tick


---

**set_all_bodies_below_linear_velocity**( _bone_name_, _linear_velocity_, _include_self=True_) → `None`

set the linear velocity of the child bodies to match that of the given parent bone

Parameters:

- **bone\_name** ( _Name_)

- **linear\_velocity** ( _Vector_)

- **include\_self** ( _bool_)



---

**set_all_bodies_below_physics_blend_weight**( _bone_name_, _physics_blend_weight_, _skip_custom_physics_type=False_, _include_self=True_) → `None`

Set all of the bones below passed in bone to be simulated

Parameters:

- **bone\_name** ( _Name_)

- **physics\_blend\_weight** ( _float_)

- **skip\_custom\_physics\_type** ( _bool_)

- **include\_self** ( _bool_)



---

**set_all_bodies_below_physics_disabled**( _bone_name_, _disabled_, _include_self=True_) → `None`

[WARNING: Chaos Only]
Set all of the bones below passed in bone to be disabled or not for the associated physics solver
Bodies will not be colliding or be part of the physics simulation.
This is different from SetAllBodiesBelowSimulatePhysics that changes bodies to Kinematic/simulated

Parameters:

- **bone\_name** ( _Name_)

- **disabled** ( _bool_)

- **include\_self** ( _bool_)



---

**set_all_bodies_below_simulate_physics**( _bone_name_, _new_simulate_, _include_self=True_) → `None`

Set all of the bones below passed in bone to be simulated

Parameters:

- **bone\_name** ( _Name_)

- **new\_simulate** ( _bool_)

- **include\_self** ( _bool_)



---

**set_all_bodies_physics_blend_weight**( _physics_blend_weight_, _skip_custom_physics_type=False_) → `None`

Set All Bodies Physics Blend Weight

Parameters:

- **physics\_blend\_weight** ( _float_)

- **skip\_custom\_physics\_type** ( _bool_)



---

**set_all_bodies_simulate_physics**( _new_simulate_) → `None`

Set bSimulatePhysics to true for all bone bodies. Does not change the component bSimulatePhysics flag.

Parameters:

**new\_simulate** ( _bool_)


---

**set_all_motors_angular_drive_params**( _spring_, _damping_, _force_limit_, _skip_custom_physics_type=False_) → `None`

Set Angular Drive motors params for all constraint instances

Parameters:

- **spring** ( _float_)

- **damping** ( _float_)

- **force\_limit** ( _float_)

- **skip\_custom\_physics\_type** ( _bool_)



---

**set_all_motors_angular_position_drive**( _enable_swing_drive_, _enable_twist_drive_, _skip_custom_physics_type=False_) → `None`

Enable or Disable AngularPositionDrive. If motor is in SLERP mode it will be turned on if either EnableSwingDrive OR EnableTwistDrive are enabled. In Twist and Swing mode the twist and the swing can be controlled individually.

Parameters:

- **enable\_swing\_drive** ( _bool_)

- **enable\_twist\_drive** ( _bool_)

- **skip\_custom\_physics\_type** ( _bool_)



---

**set_all_motors_angular_velocity_drive**( _enable_swing_drive_, _enable_twist_drive_, _skip_custom_physics_type=False_) → `None`

Enable or Disable AngularVelocityDrive. If motor is in SLERP mode it will be turned on if either EnableSwingDrive OR EnableTwistDrive are enabled. In Twist and Swing mode the twist and the swing can be controlled individually.

Parameters:

- **enable\_swing\_drive** ( _bool_)

- **enable\_twist\_drive** ( _bool_)

- **skip\_custom\_physics\_type** ( _bool_)



---

**set_allow_anim_curve_evaluation**( _allow_) → `None`

Set Allow Anim Curve Evaluation

Parameters:

**allow** ( _bool_)


---

**set_allow_cloth_actors**( _allow_) → `None`

Sets whether cloth assets should be created/simulated in this component.
This will update the conditional flag and you will want to call RecreateClothingActors for it to take effect.

Parameters:

**allow** ( _bool_) – Whether to allow the creation of cloth assets and simulation.


---

**set_allow_rigid_body_anim_node**( _allow_, _reinit_anim=True_) → `None`

Sets whether or not to allow rigid body animation nodes for this component

Parameters:

- **allow** ( _bool_)

- **reinit\_anim** ( _bool_)



---

**set_allowed_anim_curves_evaluation**( _list_, _allow_) → `None`

resets, and then only allow the following list to be allowed/disallowed

Parameters:

- **list** ( _Array_ _\_ [_Name_ _]_)

- **allow** ( _bool_)



---

**set_angular_limits**( _bone_name_, _swing1_limit_angle_, _twist_limit_angle_, _swing2_limit_angle_) → `None`

Sets the Angular Motion Ranges for a named constraint

Parameters:

- **bone\_name** ( _Name_) – Name of bone to adjust constraint ranges for

- **swing1\_limit\_angle** ( _float_) – Size of limit in degrees, 0 means locked, 180 means free

- **twist\_limit\_angle** ( _float_) – Size of limit in degrees, 0 means locked, 180 means free

- **swing2\_limit\_angle** ( _float_) – Size of limit in degrees, 0 means locked, 180 means free



---

**set_anim_blueprint**( _new_class:Class_) → `None`

deprecated: ‘set\_anim\_blueprint’ was renamed to ‘set\_anim\_instance\_class’.


---

**set_anim_class**( _new_class:Class_) → `None`

deprecated: ‘set\_anim\_class’ was renamed to ‘set\_anim\_instance\_class’.


---

**set_anim_instance_class**( _new_class_) → `None`

Set the anim instance class. Clears and re-initializes the anim instance with the new class and sets animation mode to ‘AnimationBlueprint’
This function will fail with a warning if it is called while the current anim instance is evaluating (e.g. from an anim notify).

Parameters:

**new\_class** ( _type_ _(_ _Class_ _)_)


---

**set_animation**( _new_anim_to_play_) → `NoneAnimation play functions`

- These changes status of animation instance, which is transient data, which means it won’t serialize with this component

- Because of that reason, it is not safe to be used during construction script

- Please use OverrideAnimationData for construction script. That will override AnimationData to be serialized


Parameters:

**new\_anim\_to\_play** ( _AnimationAsset_)


---

**set_animation_mode**( _animation_mode_, _force_init_anim_script_instance=True_) → `None`

Set the Animation Mode

Parameters:

- **animation\_mode** ( _AnimationMode_) – : Requested AnimationMode

- **force\_init\_anim\_script\_instance** ( _bool_) – : Init AnimScriptInstance if the AnimationMode is AnimationBlueprint even if the new animation mode is the same as current (this allows to use BP construction script to do this)



---

**set_body_notify_rigid_body_collision**( _new_notify_rigid_body_collision_, _bone_name='None'_) → `None`

Changes the value of bNotifyRigidBodyCollision for a given body

Parameters:

- **new\_notify\_rigid\_body\_collision** ( _bool_) – The value to assign to bNotifyRigidBodyCollision

- **bone\_name** ( _Name_) – Name of the body to turn hit notifies on/off. None implies root body



---

**set_body_simulate_physics**( _bone_name_, _simulate_) → `None`

Set a single bone to be simulated (or not)

Parameters:

- **bone\_name** ( _Name_)

- **simulate** ( _bool_)



---

**set_cloth_max_distance_scale**( _scale_) → `None`

Set Cloth Max Distance Scale

Parameters:

**scale** ( _float_)


---

**set_constraint_profile**( _joint_name_, _profile_name_, _default_if_not_found=False_) → `None`

Sets the constraint profile properties (limits, motors, etc…) to match the constraint profile as defined in the physics asset. If profile name is not found the joint is set to use the default constraint profile.

Parameters:

- **joint\_name** ( _Name_)

- **profile\_name** ( _Name_)

- **default\_if\_not\_found** ( _bool_)



---

**set_constraint_profile_for_all**( _profile_name_, _default_if_not_found=False_) → `None`

Sets the constraint profile properties (limits, motors, etc…) to match the constraint profile as defined in the physics asset for all constraints. If profile name is not found the joint is set to use the default constraint profile.

Parameters:

- **profile\_name** ( _Name_)

- **default\_if\_not\_found** ( _bool_)



---

**set_disable_anim_curves**( _disable_anim_curves_) → `None`

Set Disable Anim Curves

Parameters:

**disable\_anim\_curves** ( _bool_)


---

**set_enable_animation**( _new_enable_animation_) → `None`

Whether the built-in animation of this component should run when the component ticks. See USkeletalMeshComponent::bEnableAnimation for more details.
Note that this call defers setting the flag to the end of the frame as the flag cannot change during world ticking (as other tasks may be in flight)

Parameters:

**new\_enable\_animation** ( _bool_)


---

**set_enable_body_gravity**( _enable_gravity_, _bone_name_) → `None`

Enables or disables gravity for the given bone.
NAME\_None indicates the root body will be edited.
If the bone name given is otherwise invalid, nothing happens.

Parameters:

- **enable\_gravity** ( _bool_) – Whether gravity should be enabled or disabled.

- **bone\_name** ( _Name_) – The name of the bone to modify.



---

**set_enable_gravity_on_all_bodies_below**( _enable_gravity_, _bone_name_, _include_self=True_) → `None`

Enables or disables gravity to all bodies below the given bone.
NAME\_None indicates all bodies will be edited.
In that case, consider using UPrimitiveComponent::EnableGravity.

Parameters:

- **enable\_gravity** ( _bool_) – Whether gravity should be enabled or disabled.

- **bone\_name** ( _Name_) – The name of the top most bone.

- **include\_self** ( _bool_) – Whether the bone specified should be edited.



---

**set_enable_per_poly_collision**( _enable_per_poly_collision_) → `None`

Enables or disables per poly collision. This will recreate the physics state.

Parameters:

**enable\_per\_poly\_collision** ( _bool_)


---

**set_enable_physics_blending**( _new_blend_physics_) → `None`

Disable physics blending of bones \*

Parameters:

**new\_blend\_physics** ( _bool_)


---

**set_layer_overlay**( _class_:Class_) → `None`

deprecated: ‘set\_layer\_overlay’ was renamed to ‘link\_anim\_class\_layers’.


---

**set_morph_target**( _morph_target_name_, _value_, _remove_zero_weight=True_) → `None`

Set Morph Target with Name and Value(0-1)

Parameters:

- **morph\_target\_name** ( _Name_)

- **value** ( _float_)

- **remove\_zero\_weight** ( _bool_) – : Used by editor code when it should stay in the active list with zero weight



---

**set_notify_rigid_body_collision_below**( _new_notify_rigid_body_collision_, _bone_name='None'_, _include_self=True_) → `None`

Changes the value of bNotifyRigidBodyCollision on all bodies below a given bone

Parameters:

- **new\_notify\_rigid\_body\_collision** ( _bool_) – The value to assign to bNotifyRigidBodyCollision

- **bone\_name** ( _Name_) – Name of the body to turn hit notifies on (and below)

- **include\_self** ( _bool_) – Whether to modify the given body (useful for roots with multiple children)



---

**set_override_post_process_anim_bp**( _post_process_anim_blueprint_, _reinit_anim_instances=True_) → `None`

Set the post-processing AnimBP to be used for this skeletal mesh component.
In case an override post-processing AnimBP is set, the one set in skeletal mesh asset will be ignored and not used.

Parameters:

- **post\_process\_anim\_blueprint** ( _type_ _(_ _Class_ _)_)

- **reinit\_anim\_instances** ( _bool_) – Can be false when called e.g. from the construction script in a Blueprint. True when this is called while the game is running and the anim instances need to be re-initialized.



---

**set_physics_blend_weight**( _physics_blend_weight_) → `None`

This is global set up for setting physics blend weight
This does multiple things automatically
If PhysicsBlendWeight == 1.f, it will enable Simulation, and if PhysicsBlendWeight == 0.f, it will disable Simulation.
Also it will respect each body’s setup, so if the body is fixed, it won’t simulate. Vice versa
So if you’d like all bodies to change manually, do not use this function, but SetAllBodiesPhysicsBlendWeight

Parameters:

**physics\_blend\_weight** ( _float_)


---

**set_play_rate**( _rate_) → `NoneAnimation play functions`

- These changes status of animation instance, which is transient data, which means it won’t serialize with this component

- Because of that reason, it is not safe to be used during construction script

- Please use OverrideAnimationData for construction script. That will override AnimationData to be serialized


Parameters:

**rate** ( _float_)


---

**set_position**( _pos_, _fire_notifies=True_) → `NoneAnimation play functions`

- These changes status of animation instance, which is transient data, which means it won’t serialize with this component

- Because of that reason, it is not safe to be used during construction script

- Please use OverrideAnimationData for construction script. That will override AnimationData to be serialized


Parameters:

- **pos** ( _float_)

- **fire\_notifies** ( _bool_)



---

**set_skeletal_mesh_asset**( _new_mesh_) → `None`

Set the SkeletalMesh rendered for this mesh.

Parameters:

**new\_mesh** ( _SkeletalMesh_)


---

**set_sub_instance_class_by_tag**( _tag:Name_, _class_:Class_) → `None`

deprecated: ‘set\_sub\_instance\_class\_by\_tag’ was renamed to ‘link\_anim\_graph\_by\_tag’.


---

**set_update_animation_in_editor**( _new_update_state_) → `None`

Sets whether or not to force tick component in order to update animation and refresh transform for this component
This is supported only in the editor

Parameters:

**new\_update\_state** ( _bool_)


---

**set_update_cloth_in_editor**( _new_update_state_) → `None`

Sets whether or not to animate cloth in the editor. Requires Update Animation In Editor to also be true.
This is supported only in the editor

Parameters:

**new\_update\_state** ( _bool_)


---

_property_ `skeletal_mesh_asset`: SkeletalMesh

[Read-Write]

**Type:**

( SkeletalMesh)


---

_property_ `skip_bounds_update_when_interpolating`: bool

[Read-Write] Whether to skip bounds update when interpolating. Bounds are updated to the target interpolation pose only on ticks when they are evaluated.

**Type:**

( bool)


---

_property_ `skip_kinematic_update_when_interpolating`: bool

[Read-Write] Whether to skip UpdateKinematicBonesToAnim() when interpolating. Kinematic bones are updated to the target interpolation pose only on ticks when they are evaluated.

**Type:**

( bool)


---

**snapshot_pose**( _snapshot_) → `PoseSnapshot`

Takes a snapshot of this skeletal mesh component’s pose and saves it to the specified snapshot.
The snapshot is taken at the current LOD, so if for example you took the snapshot at LOD1
and then used it at LOD0 any bones not in LOD1 will use the reference pose

Parameters:

**snapshot** ( _PoseSnapshot_)

Returns:

snapshot (PoseSnapshot):

Return type:

PoseSnapshot


---

**stop**() → `None`

Animation play functions
\\*
\\* These changes status of animation instance, which is transient data, which means it won’t serialize with this component
\\* Because of that reason, it is not safe to be used during construction script
\\* Please use OverrideAnimationData for construction script. That will override AnimationData to be serialized


---

**suspend_clothing_simulation**() → `None`

Stops simulating clothing, but does not show clothing ref pose. Keeps the last known simulation state


---

_property_ `teleport_distance_threshold`: float

[Read-Write] Conduct teleportation if the character’s movement is greater than this threshold in 1 frame.
Zero or negative values will skip the check.
You can also do force teleport manually using ForceNextUpdateTeleport() / ForceNextUpdateTeleportAndReset().

**Type:**

( float)


---

_property_ `teleport_rotation_threshold`: float

[Read-Write] Rotation threshold in degrees, ranging from 0 to 180.
Conduct teleportation if the character’s rotation is greater than this threshold in 1 frame.
Zero or negative values will skip the check.

**Type:**

( float)


---

**term_bodies_below**( _parent_bone_name_) → `None`

Terminate physics on all bodies below the named bone, effectively disabling collision forever. If you terminate, you won’t be able to re-init later.

Parameters:

**parent\_bone\_name** ( _Name_)


---

**toggle_disable_post_process_blueprint**() → `None`

Toggles whether the post process blueprint will run for this component


---

**unbind_cloth_from_leader_pose_component**( _restore_simulation_space=True_) → `None`

If this component has a valid LeaderPoseComponent and has previously had its cloth bound to the
MCP, this function will unbind the cloth and resume simulation.

Parameters:

**restore\_simulation\_space** ( _bool_) – if true and the leader pose cloth was originally simulating in world space, we will restore this setting. This will cause the leader component to reset which may be undesirable.


---

**unbind_cloth_from_master_pose_component**( _restore_simulation_space:bool=True_) → `None`

deprecated: ‘unbind\_cloth\_from\_master\_pose\_component’ was renamed to ‘unbind\_cloth\_from\_leader\_pose\_component’.


---

**unlink_anim_class_layers**( _class__) → `None`

Runs through all layer nodes, attempting to find layer nodes that are currently running the specified class, then resets each to its default value.
State sharing rules are as with SetLayerOverlay.
If InClass is null, does nothing.

Parameters:

**class** ( _type_ _(_ _Class_ _)_)


---

_property_ `update_joints_from_animation`: bool

[Read-Write] If we should pass joint position to joints each frame, so that they can be used by motorized joints to drive the
ragdoll based on the animation.

**Type:**

( bool)


---

_property_ `update_mesh_when_kinematic`: bool

[Read-Write] If true, then the physics bodies will be used to drive the skeletal mesh even when they are
kinematic (not simulating), otherwise the skeletal mesh will be driven by the animation input
when the bodies are kinematic

**Type:**

( bool)


---

_property_ `wait_for_parallel_cloth_task`: bool

[Read-Write] Whether we should stall the Cloth tick task until the cloth simulation is complete. This is required if we want up-to-date
cloth data on the game thread, for example if we want to generate particles at cloth vertices.

**Type:**

( bool)

### Table of Contents

- `unreal.SkeletalMeshComponent`
  - `SkeletalMeshComponent`
    - `SkeletalMeshComponent.accumulate_all_bodies_below_physics_blend_weight()`
    - `SkeletalMeshComponent.add_cloth_collision_source()`
    - `SkeletalMeshComponent.add_force_to_all_bodies_below()`
    - `SkeletalMeshComponent.add_impulse_to_all_bodies_below()`
    - `SkeletalMeshComponent.allow_anim_curve_evaluation()`
    - `SkeletalMeshComponent.allow_cloth_actors`
    - `SkeletalMeshComponent.anim_blueprint_generated_class`
    - `SkeletalMeshComponent.anim_class`
    - `SkeletalMeshComponent.animation_blueprint`
    - `SkeletalMeshComponent.animation_data`
    - `SkeletalMeshComponent.animation_mode`
    - `SkeletalMeshComponent.b_propagate_curves_to_slaves`
    - `SkeletalMeshComponent.bind_cloth_to_leader_pose_component()`
    - `SkeletalMeshComponent.bind_cloth_to_master_pose_component()`
    - `SkeletalMeshComponent.break_constraint()`
    - `SkeletalMeshComponent.clear_layer_overlay()`
    - `SkeletalMeshComponent.clear_morph_targets()`
    - `SkeletalMeshComponent.cloth_blend_weight`
    - `SkeletalMeshComponent.cloth_geometry_scale`
    - `SkeletalMeshComponent.cloth_max_distance_scale`
    - `SkeletalMeshComponent.cloth_teleport_mode`
    - `SkeletalMeshComponent.cloth_velocity_scale`
    - `SkeletalMeshComponent.collide_with_attached_children`
    - `SkeletalMeshComponent.collide_with_environment`
    - `SkeletalMeshComponent.default_animating_rig_override`
    - `SkeletalMeshComponent.defer_kinematic_bone_update`
    - `SkeletalMeshComponent.disable_cloth_simulation`
    - `SkeletalMeshComponent.disable_post_process_blueprint`
    - `SkeletalMeshComponent.enable_animation`
    - `SkeletalMeshComponent.enable_per_poly_collision`
    - `SkeletalMeshComponent.enable_physics_on_dedicated_server`
    - `SkeletalMeshComponent.find_constraint_bone_name()`
    - `SkeletalMeshComponent.force_cloth_next_update_teleport()`
    - `SkeletalMeshComponent.force_cloth_next_update_teleport_and_reset()`
    - `SkeletalMeshComponent.force_collision_update`
    - `SkeletalMeshComponent.get_allow_cloth_actors()`
    - `SkeletalMeshComponent.get_allow_rigid_body_anim_node()`
    - `SkeletalMeshComponent.get_allowed_anim_curve_evaluate()`
    - `SkeletalMeshComponent.get_anim_instance()`
    - `SkeletalMeshComponent.get_animation_mode()`
    - `SkeletalMeshComponent.get_bone_linear_velocity()`
    - `SkeletalMeshComponent.get_bone_mass()`
    - `SkeletalMeshComponent.get_closest_point_on_physics_asset()`
    - `SkeletalMeshComponent.get_cloth_max_distance_scale()`
    - `SkeletalMeshComponent.get_clothing_simulation_interactor()`
    - `SkeletalMeshComponent.get_constraint_by_name()`
    - `SkeletalMeshComponent.get_constraints()`
    - `SkeletalMeshComponent.get_constraints_from_body()`
    - `SkeletalMeshComponent.get_current_joint_angles()`
    - `SkeletalMeshComponent.get_curve_value()`
    - `SkeletalMeshComponent.get_default_animating_rig()`
    - `SkeletalMeshComponent.get_disable_anim_curves()`
    - `SkeletalMeshComponent.get_float_attribute()`
    - `SkeletalMeshComponent.get_float_attribute_ref()`
    - `SkeletalMeshComponent.get_integer_attribute()`
    - `SkeletalMeshComponent.get_integer_attribute_ref()`
    - `SkeletalMeshComponent.get_layer_sub_instance_by_class()`
    - `SkeletalMeshComponent.get_layer_sub_instance_by_group()`
    - `SkeletalMeshComponent.get_linked_anim_graph_instance_by_tag()`
    - `SkeletalMeshComponent.get_linked_anim_graph_instances_by_tag()`
    - `SkeletalMeshComponent.get_linked_anim_layer_instance_by_class()`
    - `SkeletalMeshComponent.get_linked_anim_layer_instance_by_group()`
    - `SkeletalMeshComponent.get_morph_target()`
    - `SkeletalMeshComponent.get_play_rate()`
    - `SkeletalMeshComponent.get_position()`
    - `SkeletalMeshComponent.get_post_process_instance()`
    - `SkeletalMeshComponent.get_skeletal_center_of_mass()`
    - `SkeletalMeshComponent.get_skeletal_mesh_asset()`
    - `SkeletalMeshComponent.get_string_attribute()`
    - `SkeletalMeshComponent.get_string_attribute_ref()`
    - `SkeletalMeshComponent.get_sub_instance_by_tag()`
    - `SkeletalMeshComponent.get_sub_instances_by_tag()`
    - `SkeletalMeshComponent.get_transform_attribute()`
    - `SkeletalMeshComponent.get_transform_attribute_ref()`
    - `SkeletalMeshComponent.global_anim_rate_scale`
    - `SkeletalMeshComponent.has_valid_animation_instance()`
    - `SkeletalMeshComponent.is_body_gravity_enabled()`
    - `SkeletalMeshComponent.is_clothing_simulation_suspended()`
    - `SkeletalMeshComponent.is_playing()`
    - `SkeletalMeshComponent.k2_set_anim_instance_class()`
    - `SkeletalMeshComponent.kinematic_bones_update_type`
    - `SkeletalMeshComponent.link_anim_class_layers()`
    - `SkeletalMeshComponent.link_anim_graph_by_tag()`
    - `SkeletalMeshComponent.no_skeleton_update`
    - `SkeletalMeshComponent.on_anim_initialized`
    - `SkeletalMeshComponent.on_constraint_broken`
    - `SkeletalMeshComponent.on_plastic_deformation`
    - `SkeletalMeshComponent.override_animation_data()`
    - `SkeletalMeshComponent.pause_anims`
    - `SkeletalMeshComponent.physics_transform_update_mode`
    - `SkeletalMeshComponent.play()`
    - `SkeletalMeshComponent.play_animation()`
    - `SkeletalMeshComponent.post_process_anim_bplod_threshold`
    - `SkeletalMeshComponent.propagate_curves_to_followers`
    - `SkeletalMeshComponent.recreate_clothing_actors()`
    - `SkeletalMeshComponent.remove_cloth_collision_source()`
    - `SkeletalMeshComponent.remove_cloth_collision_sources()`
    - `SkeletalMeshComponent.reset_after_teleport`
    - `SkeletalMeshComponent.reset_all_bodies_simulate_physics()`
    - `SkeletalMeshComponent.reset_allowed_anim_curve_evaluation()`
    - `SkeletalMeshComponent.reset_anim_instance_dynamics()`
    - `SkeletalMeshComponent.reset_cloth_collision_sources()`
    - `SkeletalMeshComponent.reset_cloth_teleport_mode()`
    - `SkeletalMeshComponent.resume_clothing_simulation()`
    - `SkeletalMeshComponent.set_all_bodies_below_linear_velocity()`
    - `SkeletalMeshComponent.set_all_bodies_below_physics_blend_weight()`
    - `SkeletalMeshComponent.set_all_bodies_below_physics_disabled()`
    - `SkeletalMeshComponent.set_all_bodies_below_simulate_physics()`
    - `SkeletalMeshComponent.set_all_bodies_physics_blend_weight()`
    - `SkeletalMeshComponent.set_all_bodies_simulate_physics()`
    - `SkeletalMeshComponent.set_all_motors_angular_drive_params()`
    - `SkeletalMeshComponent.set_all_motors_angular_position_drive()`
    - `SkeletalMeshComponent.set_all_motors_angular_velocity_drive()`
    - `SkeletalMeshComponent.set_allow_anim_curve_evaluation()`
    - `SkeletalMeshComponent.set_allow_cloth_actors()`
    - `SkeletalMeshComponent.set_allow_rigid_body_anim_node()`
    - `SkeletalMeshComponent.set_allowed_anim_curves_evaluation()`
    - `SkeletalMeshComponent.set_angular_limits()`
    - `SkeletalMeshComponent.set_anim_blueprint()`
    - `SkeletalMeshComponent.set_anim_class()`
    - `SkeletalMeshComponent.set_anim_instance_class()`
    - `SkeletalMeshComponent.set_animation()`
    - `SkeletalMeshComponent.set_animation_mode()`
    - `SkeletalMeshComponent.set_body_notify_rigid_body_collision()`
    - `SkeletalMeshComponent.set_body_simulate_physics()`
    - `SkeletalMeshComponent.set_cloth_max_distance_scale()`
    - `SkeletalMeshComponent.set_constraint_profile()`
    - `SkeletalMeshComponent.set_constraint_profile_for_all()`
    - `SkeletalMeshComponent.set_disable_anim_curves()`
    - `SkeletalMeshComponent.set_enable_animation()`
    - `SkeletalMeshComponent.set_enable_body_gravity()`
    - `SkeletalMeshComponent.set_enable_gravity_on_all_bodies_below()`
    - `SkeletalMeshComponent.set_enable_per_poly_collision()`
    - `SkeletalMeshComponent.set_enable_physics_blending()`
    - `SkeletalMeshComponent.set_layer_overlay()`
    - `SkeletalMeshComponent.set_morph_target()`
    - `SkeletalMeshComponent.set_notify_rigid_body_collision_below()`
    - `SkeletalMeshComponent.set_override_post_process_anim_bp()`
    - `SkeletalMeshComponent.set_physics_blend_weight()`
    - `SkeletalMeshComponent.set_play_rate()`
    - `SkeletalMeshComponent.set_position()`
    - `SkeletalMeshComponent.set_skeletal_mesh_asset()`
    - `SkeletalMeshComponent.set_sub_instance_class_by_tag()`
    - `SkeletalMeshComponent.set_update_animation_in_editor()`
    - `SkeletalMeshComponent.set_update_cloth_in_editor()`
    - `SkeletalMeshComponent.skeletal_mesh_asset`
    - `SkeletalMeshComponent.skip_bounds_update_when_interpolating`
    - `SkeletalMeshComponent.skip_kinematic_update_when_interpolating`
    - `SkeletalMeshComponent.snapshot_pose()`
    - `SkeletalMeshComponent.stop()`
    - `SkeletalMeshComponent.suspend_clothing_simulation()`
    - `SkeletalMeshComponent.teleport_distance_threshold`
    - `SkeletalMeshComponent.teleport_rotation_threshold`
    - `SkeletalMeshComponent.term_bodies_below()`
    - `SkeletalMeshComponent.toggle_disable_post_process_blueprint()`
    - `SkeletalMeshComponent.unbind_cloth_from_leader_pose_component()`
    - `SkeletalMeshComponent.unbind_cloth_from_master_pose_component()`
    - `SkeletalMeshComponent.unlink_anim_class_layers()`
    - `SkeletalMeshComponent.update_joints_from_animation`
    - `SkeletalMeshComponent.update_mesh_when_kinematic`
    - `SkeletalMeshComponent.wait_for_parallel_cloth_task`