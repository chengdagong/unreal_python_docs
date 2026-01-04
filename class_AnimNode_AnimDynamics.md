# unreal.AnimNode_AnimDynamics

```python
class unreal.AnimNode_AnimDynamics(component_pose:ComponentSpacePoseLink=\[\], lod_threshold:int=0, alpha_input_type:AnimAlphaInputType=Ellipsis, alpha_bool_enabled:bool=False, alpha:float=0.0, alpha_scale_bias:InputScaleBias=Ellipsis, alpha_bool_blend:InputAlphaBoolBlend=Ellipsis, alpha_curve_name:Name='None', alpha_scale_bias_clamp:InputScaleBiasClamp=Ellipsis, linear_damping_override:float=0.0, angular_damping_override:float=0.0, gravity_scale:float=0.0, gravity_override:Vector=Ellipsis, linear_spring_constant:float=0.0, angular_spring_constant:float=0.0, angular_bias_override:float=0.0, simulation_space:AnimPhysSimSpaceType=Ellipsis, use_gravity_override:bool=False)
```


**Bases:** ``AnimNode_SkeletalControlBase``


Anim Node Anim Dynamics

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_AnimDynamics.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alpha` (float): [Read-Write] Current strength of the skeletal control

- `alpha_bool_blend` (InputAlphaBoolBlend): [Read-Write]

- `alpha_bool_enabled` (bool): [Read-Write]

- `alpha_curve_name` (Name): [Read-Write]

- `alpha_input_type` (AnimAlphaInputType): [Read-Write]

- `alpha_scale_bias` (InputScaleBias): [Read-Write]

- `alpha_scale_bias_clamp` (InputScaleBiasClamp): [Read-Write]

- `angular_bias_override` (float): [Read-Write] Overridden angular bias value
Angular bias is essentially a twist reduction for chain forces and defaults to a value to keep chains stability
in check. When using single-body systems sometimes angular forces will look like they are “catching-up” with
the mesh, if that’s the case override this and push it towards 1.0f until it settles correctly

- `angular_damping_override` (float): [Read-Write] Overridden angular damping value. The default is 0.7. Values below 0.7 won’t have an effect.

- `angular_spring` (bool): [Read-Write] If true the body will attempt to align itself with the specified angular target

- `angular_spring_constant` (float): [Read-Write] Spring constant to use when calculating angular springs, higher values mean a stronger spring.
You need to enable the Angular Spring checkbox for this to have an effect.
Note: Make sure to also set the Angular Target Axis and Angular Target in the Constraint Setup for this to have an effect.

- `bound_bone` (BoneReference): [Read-Write] The bone to attach the physics body to, if bChain is true this is the top of the chain

- `chain` (bool): [Read-Write] Set to true to use the solver to simulate a connected chain

- `chain_end` (BoneReference): [Read-Write] If bChain is true this is the bottom of the chain, otherwise ignored

- `component_applied_linear_acc_clamp` (Vector): [Read-Write] When using non-world-space sim, this is an overall clamp on acceleration derived from ComponentLinearAccScale and ComponentLinearVelScale, to ensure it is not too large.

- `component_linear_acc_scale` (Vector): [Read-Write] When using non-world-space sim, this controls how much of the components world-space acceleration is passed on to the local-space simulation.

- `component_linear_vel_scale` (Vector): [Read-Write] When using non-world-space sim, this applies a ‘drag’ to the bodies in the local space simulation, based on the components world-space velocity.

- `component_pose` (ComponentSpacePoseLink): [Read-Write] Input link

- `do_eval` (bool): [Read-Write] If true we will perform bone transform evaluation, otherwise skip - allows visualization of the initial anim state compared to the physics sim

- `do_update` (bool): [Read-Write] If true we will perform physics update, otherwise skip - allows visualization of the initial state of the bodies

- `enable_wind` (bool): [Read-Write] Whether or not wind is enabled for the bodies in this simulation

- `external_force` (Vector): [Read-Write] An external force to apply to all bodies in the simulation when ticked, specified in world space

- `gravity_override` (Vector): [Read-Write] Gravity Override Value

- `gravity_override_in_sim_space` (bool): [Read-Write] If true the gravity override value is defined in simulation space, by default it is in world space

- `gravity_scale` (float): [Read-Write] Scale for gravity, higher values increase forces due to gravity

- `linear_damping_override` (float): [Read-Write] Overridden linear damping value. The default is 0.7. Values below 0.7 won’t have an effect.

- `linear_spring` (bool): [Read-Write] If true the body will attempt to spring back to its initial position

- `linear_spring_constant` (float): [Read-Write] Spring constant to use when calculating linear springs, higher values mean a stronger spring.
You need to enable the Linear Spring checkbox for this to have an effect.

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

- `num_solver_iterations_post_update` (int32): [Read-Write] Number of update passes on the linear and angular limits after we solve the position of the bodies, recommended to be around a quarter of NumSolverIterationsPreUpdate

- `num_solver_iterations_pre_update` (int32): [Read-Write] Number of update passes on the linear and angular limits before we solve the position of the bodies recommended to be four times the value of NumSolverIterationsPostUpdate

- `override_angular_bias` (bool): [Read-Write] If true, the override value will be used for the angular bias for bodies in this node.
Angular bias is essentially a twist reduction for chain forces and defaults to a value to keep chains stability
in check. When using single-body systems sometimes angular forces will look like they are “catching-up” with
the mesh, if that’s the case override this and push it towards 1.0f until it settles correctly

- `override_angular_damping` (bool): [Read-Write] If true, the override value will be used for angular damping

- `override_linear_damping` (bool): [Read-Write] If true, the override value will be used for linear damping

- `physics_body_definitions` (Array[AnimPhysBodyDefinition]): [Read-Write]

- `planar_limits` (Array[AnimPhysPlanarLimit]): [Read-Write] List of available planar limits for this node

- `relative_space_bone` (BoneReference): [Read-Write] When in BoneRelative sim space, the simulation will use this bone as the origin

- `retargeting_settings` (RotationRetargetingInfo): [Read-Write] The settings for rotation retargeting

- `sim_space_settings` (AnimPhysSimSpaceSettings): [Read-Write] Settings for the system which passes motion of the simulation’s space
into the simulation. This allows the simulation to pass a
fraction of the world space motion onto the bodies which allows Bone-Space
and Component-Space simulations to react to world-space movement in a
controllable way.
This system is a superset of the functionality provided by ComponentLinearAccScale,
ComponentLinearVelScale, and ComponentAppliedLinearAccClamp. In general
you should not have both systems enabled.

- `simulation_space` (AnimPhysSimSpaceType): [Read-Write] The space used to run the simulation

- `spherical_limits` (Array[AnimPhysSphericalLimit]): [Read-Write] List of available spherical limits for this node

- `use_gravity_override` (bool): [Read-Write] Use gravity override value vs gravity scale

- `use_planar_limit` (bool): [Read-Write] Whether to evaluate planar limits

- `use_spherical_limits` (bool): [Read-Write] Whether to evaluate spherical limits

- `wind_scale` (float): [Read-Write] Scale to apply to calculated wind velocities in the solver



---

_property_ `angular_bias_override`: float

[Read-Write] Overridden angular bias value
Angular bias is essentially a twist reduction for chain forces and defaults to a value to keep chains stability
in check. When using single-body systems sometimes angular forces will look like they are “catching-up” with
the mesh, if that’s the case override this and push it towards 1.0f until it settles correctly

**Type:**

( float)


---

_property_ `angular_damping_override`: float

[Read-Write] Overridden angular damping value. The default is 0.7. Values below 0.7 won’t have an effect.

**Type:**

( float)


---

_property_ `angular_spring_constant`: float

[Read-Write] Spring constant to use when calculating angular springs, higher values mean a stronger spring.
You need to enable the Angular Spring checkbox for this to have an effect.
Note: Make sure to also set the Angular Target Axis and Angular Target in the Constraint Setup for this to have an effect.

**Type:**

( float)


---

_property_ `gravity_override`: Vector

[Read-Write] Gravity Override Value

**Type:**

( Vector)


---

_property_ `gravity_scale`: float

[Read-Write] Scale for gravity, higher values increase forces due to gravity

**Type:**

( float)


---

_property_ `linear_damping_override`: float

[Read-Write] Overridden linear damping value. The default is 0.7. Values below 0.7 won’t have an effect.

**Type:**

( float)


---

_property_ `linear_spring_constant`: float

[Read-Write] Spring constant to use when calculating linear springs, higher values mean a stronger spring.
You need to enable the Linear Spring checkbox for this to have an effect.

**Type:**

( float)


---

_property_ `simulation_space`: AnimPhysSimSpaceType

[Read-Write] The space used to run the simulation

**Type:**

( AnimPhysSimSpaceType)


---

_property_ `use_gravity_override`: bool

[Read-Write] Use gravity override value vs gravity scale

**Type:**

( bool)

### Table of Contents

- `unreal.AnimNode_AnimDynamics`
  - `AnimNode_AnimDynamics`
    - `AnimNode_AnimDynamics.angular_bias_override`
    - `AnimNode_AnimDynamics.angular_damping_override`
    - `AnimNode_AnimDynamics.angular_spring_constant`
    - `AnimNode_AnimDynamics.gravity_override`
    - `AnimNode_AnimDynamics.gravity_scale`
    - `AnimNode_AnimDynamics.linear_damping_override`
    - `AnimNode_AnimDynamics.linear_spring_constant`
    - `AnimNode_AnimDynamics.simulation_space`
    - `AnimNode_AnimDynamics.use_gravity_override`