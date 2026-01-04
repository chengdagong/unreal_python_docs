# unreal.AnimNode_RigidBodyWithControl

```python
class unreal.AnimNode_RigidBodyWithControl(component_pose:ComponentSpacePoseLink=\[\], lod_threshold:int=0, alpha_input_type:AnimAlphaInputType=Ellipsis, alpha_bool_enabled:bool=False, alpha:float=0.0, alpha_scale_bias:InputScaleBias=Ellipsis, alpha_bool_blend:InputAlphaBoolBlend=Ellipsis, alpha_curve_name:Name='None', alpha_scale_bias_clamp:InputScaleBiasClamp=Ellipsis)
```


**Bases:** ``AnimNode_SkeletalControlBase``


Controller that simulates physics based on the physics asset of the skeletal mesh component

**C++ Source:**

- **Plugin**: PhysicsControl

- **Module**: PhysicsControl

- **File**: AnimNode\_RigidBodyWithControl.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `additional_controls_and_body_modifiers` (PhysicsControlAndBodyModifierCreationDatas): [Read-Write] Controls and modifiers that should be created, in addition to those made as part of the limb setup.

- `additional_sets` (PhysicsControlSetUpdates): [Read-Write] Allows additional sets of controls or modifiers to be created, and existing sets to be modified

- `alpha` (float): [Read-Write] Current strength of the skeletal control

- `alpha_bool_blend` (InputAlphaBoolBlend): [Read-Write]

- `alpha_bool_enabled` (bool): [Read-Write]

- `alpha_curve_name` (Name): [Read-Write]

- `alpha_input_type` (AnimAlphaInputType): [Read-Write]

- `alpha_scale_bias` (InputScaleBias): [Read-Write]

- `alpha_scale_bias_clamp` (InputScaleBiasClamp): [Read-Write]

- `base_bone_ref` (BoneReference): [Read-Write] Matters if SimulationSpace is BaseBone

- `bone_to_body_name_map` (Map[Name, Name]): [Read-Write] A map of bone names to “body” names, the latter being used to assign names to controls/modifiers.
This is optional - so if there is no mapping for a bone, then its name will be used directly when
creating controls. The two main benefits of this are (1) to generate consistently named controls
even on different skeletons and (2) to make it easier to refer to individual controls, without needing
to refer to the skeleton.

- `cached_bounds_scale` (float): [Read-Write] Scale of cached bounds (vs. actual bounds) used for obtaining the list of objects we might collide with.
Increasing this may improve performance, but overlaps may not work as well.
(A value of 1.0 effectively disables cached bounds).

- `calculate_velocities_for_world_geometry` (bool): [Read-Write] Whether or not to calculate velocities for world geometry. Note that if the simulation space is
not set to world, then even static objects “should” have velocities calculated. There is a cost
associated with calculating velocities, but without them there may be more penetration between
the simulated objects and the world.

- `character_setup_data` (PhysicsControlCharacterSetupData): [Read-Write] Setup data for creating the main controls (world- and parent-space) and modifiers, based on splitting the
skeleton up into limbs.

- `component_applied_linear_acc_clamp` (Vector): [Read-Write] When using non-world-space sim, this is an overall clamp on acceleration derived from ComponentLinearAccScale and ComponentLinearVelScale, to ensure it is not too large.

- `component_linear_acc_scale` (Vector): [Read-Write] When using non-world-space sim, this controls how much of the components world-space acceleration is passed on to the local-space simulation.

- `component_linear_vel_scale` (Vector): [Read-Write] When using non-world-space sim, this applies a ‘drag’ to the bodies in the local space simulation, based on the components world-space velocity.

- `component_pose` (ComponentSpacePoseLink): [Read-Write] Input link

- `constraint_profile` (Name): [Read-Write] The constraint profile to use on all the joints in the physics asset. Will be applied when
the profile name changes.

- `control_and_modifier_parameters` (PhysicsControlControlAndModifierParameters): [Read-Write] Controls that should be applied each frame, and can be expected to change. Note that if these
stop being passed in then the controls and modifiers will return to their normal/original state.

- `control_and_modifier_updates` (PhysicsControlControlAndModifierUpdates): [Read-Write] Updates to controls that can be applied. Note that these update the normal/original state.

- `control_profile` (Name): [Read-Write] The control profile to use. Will be applied when the profile name changes. To force it to be invoked again,
either change the profile to something else for a frame, or call InvokeControlProfile.

- `control_targets` (RigidBodyControlTargets): [Read-Write] Targets that should be applied to the controls.

- `default_to_skeletal_mesh_physics_asset` (bool): [Read-Write] Use the skeletal mesh physics asset as default in case set to True. The Override Physics Asset
will always have priority over this.

- `enable_character_setup_data` (bool): [Read-Write]

- `enable_controls` (bool): [Read-Write] If false, then controls will not be created. Note that this can be exposed as a pin/bound, and then control
creation can be deferred to when the value is set to true as the node runs.

- `enable_world_geometry` (bool): [Read-Write]

- `evaluation_reset_time` (float): [Read-Write] If the node is not evaluated for this amount of time (seconds), either because a lower LOD was in use
for a while or the component was not visible, reset the simulation to the default pose on the next
evaluation. Set to 0 to disable time-based reset.

- `external_force` (Vector): [Read-Write] Applies a uniform external force in world space. This allows for easily faking inertia of movement while still simulating in component space for example

- `force_disable_collision_between_constraint_bodies` (bool): [Read-Write] Whether to allow collisions between two bodies joined by a constraint

- `freeze_incoming_pose_on_start` (bool): [Read-Write] When simulation starts, freeze incoming pose.
This is useful for ragdolls, when we want the simulation to take over.
It prevents non simulated bones from animating.

- `initial_control_and_body_modifier_updates` (PhysicsControlControlAndModifierParameters): [Read-Write] An initial set of controls that should be applied immediately after setup. This allows individual or
sets of controls/modifiers etc to be adjusted. Note that these will then be “baked” into the
controls.

- `kinematic_targets` (RigidBodyKinematicTargets): [Read-Write] Targets that should be applied to kinematic bodies that are under the influence of a body modifier.

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

- `make_kinematic_constraints` (bool): [Read-Write] If true, constraints will be made even when both objects are kinematic, in case they are subsequently
made dynamic. There may be a small performance benefit to disabling this if you know this won’t happen.

- `overlap_channel` (CollisionChannel): [Read-Write] The channel we use to find static geometry to collide with

- `override_physics_asset` (PhysicsAsset): [Read-Write] Physics asset to use. If empty use the skeletal mesh’s default physics asset. Note that this can be
changed at runtime using SetOverridePhysicsAsset in the Animation Node Functions

- `override_world_gravity` (bool): [Read-Write]

- `override_world_gravity` (Vector): [Read-Write] Override gravity

- `physics_asset_authored_skeletal_mesh` (SkeletalMesh): [Read-Write] These options configure the way constraint transforms can be modified at runtime to match the current Skeletal
Mesh. This can be useful when applying a single RBwC node to assets with different skeletons.

When the “From authored skeletal mesh” option is selected, the Position and/or Orientation of each constraint
relative to its parent bone will be changed to account for any difference in relative bone transforms
between that Skeletal Mesh and the current one. This means that if bone positions or orientations have changed
between the authored Skeletal Mesh and the one currently being animated then the constraint positions and
orientations will be updated to match. The authored Skeletal Mesh should normally be set to the same skeletal
mesh that was used when creating the physics asset. WARNING This option will do nothing if the authored
skeleton is not defined or cannot be found when the node is initialized at runtime.

When the “To default” option is selected the Position and/or Orientation of each constraint relative to its
parent bone will be set to the Position and/or Orientation of the constraint’s child bone relative to its parent
bone. This is the same as the default transform applied in the Physics Asset editing tool when a constraint is
created or ‘snapped’ to the default transform.

[WARNING]
The “To default” option can produce undesirable results and should be used with caution but may be useful
for simple assets or to minimize sudden changes in bone positions that may arise if the
authored skeleton is unavailable during the early stages of initialization. In most cases its probably more
useful to only set constraint positions to the default.

- `physics_asset_conditioning_constraint_orientation` (MapConstraintsBehaviorType): [Read-Write] Configure the way constraint orientations can be modified at runtime to match the current Skeletal Mesh.

- `physics_asset_conditioning_constraint_position` (MapConstraintsBehaviorType): [Read-Write] Configure the way constraint positions can be modified at runtime to match the current Skeletal Mesh.

- `physics_control_asset` (PhysicsControlAsset): [Read-Write] Physics control asset to use. This is optional, but if it has been set, then it will be used
during creation of controls/body modifiers. Note that this can be modified at runtime in the Animation
Blueprint via the Animation Node functions.

- `sim_space_settings` (SimSpaceSettings): [Read-Write] Settings for the system which passes motion of the simulation’s space
into the simulation. This allows the simulation to pass a
fraction of the world space motion onto the bodies which allows Bone-Space
and Component-Space simulations to react to world-space movement in a
controllable way.
This system is a superset of the functionality provided by ComponentLinearAccScale,
ComponentLinearVelScale, and ComponentAppliedLinearAccClamp. In general
you should not have both systems enabled.

- `simulation_space` (SimulationSpace): [Read-Write] What space to simulate the bodies in. This affects how velocities are generated

- `simulation_timing` (SimulationTiming): [Read-Write] \* Whether the physics simulation runs synchronously with the node’s evaluation or is run in the
\\* background until the next frame. Note that running with deferred timing can improve performance,
\\* but there will be a frame’s lag in the output (relative to the input animation), and there can
\\* be problems with handling collisions.

- `transfer_bone_velocities` (bool): [Read-Write] When simulation starts, transfer previous bone velocities (from animation)
to make transition into simulation seamless.

- `update_cache_every_frame` (bool): [Read-Write] This can be used to force the cached collision objects to be updated every frame, even when we are not
moving. This can be expensive, but may be needed if we wish to detect collisions with objects that are
moving, otherwise the cache will only be updated if/when we move.

- `use_external_cloth_collision` (bool): [Read-Write] If true, kinematic objects will be added to the simulation at runtime to represent any cloth colliders defined for the parent object.

- `world_space_minimum_scale` (float): [Read-Write] For world-space simulations, if the magnitude of the component’s 3D scale is less than
WorldSpaceMinimumScale, do not update the node.


### Table of Contents

- `unreal.AnimNode_RigidBodyWithControl`
  - `AnimNode_RigidBodyWithControl`