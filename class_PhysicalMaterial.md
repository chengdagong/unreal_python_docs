# unreal.PhysicalMaterial

```python
class unreal.PhysicalMaterial(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


Physical materials are used to define the response of a physical object when interacting dynamically with the world.

**C++ Source:**

- **Module**: PhysicsCore

- **File**: PhysicalMaterial.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `base_friction_impulse` (float): [Read-Write] A friction (positional) impulse of at least this magnitude may be applied,

regardless the normal force. This is analogous to adding only the lateral part of a
“stickiness” to a material

- `damage_modifier` (PhysicalMaterialDamageModifier): [Read-Write]

- `debug_color` (LinearColor): [Read-Write] Color used to represent this material in certain debug views (e.g. landscape collision)

- `density` (float): [Read-Write] Used with the shape of the object to calculate its mass properties. The higher the number, the heavier the object. g per cubic cm.

- `friction` (float): [Read-Write] Friction value of surface, controls how easily things can slide on this surface (0 is frictionless, higher values increase the amount of friction)

- `friction_combine_mode` (FrictionCombineMode): [Read-Write] Friction combine mode, controls how friction is computed for multiple materials.

- `override_friction_combine_mode` (bool): [Read-Write] If set we will use the FrictionCombineMode of this material, instead of the FrictionCombineMode found in the project settings.

- `override_restitution_combine_mode` (bool): [Read-Write] If set we will use the RestitutionCombineMode of this material, instead of the RestitutionCombineMode found in the project settings.

- `raise_mass_to_power` (float): [Read-Write] Used to adjust the way that mass increases as objects get larger. This is applied to the mass as calculated based on a ‘solid’ object.
In actuality, larger objects do not tend to be solid, and become more like ‘shells’ (e.g. a car is not a solid piece of metal).
Values are clamped to 1 or less.

- `restitution` (float): [Read-Write] Restitution or ‘bounciness’ of this surface, between 0 (no bounce) and 1 (outgoing velocity is same as incoming).

- `restitution_combine_mode` (FrictionCombineMode): [Read-Write] Restitution combine mode, controls how restitution is computed for multiple materials.

- `show_experimental_properties` (bool): [Read-Only] Experimental material properties are enabled via the p.PhysicalMaterial.ShowExperimentalProperties console variable.

NOTE: These are \_experimental\_ properties which may change. Use at your own risk!

- `sleep_angular_velocity_threshold` (float): [Read-Write] How low the angular velocity can be before solver puts body to sleep.

- `sleep_counter_threshold` (int32): [Read-Write] How many ticks we can be under thresholds for before solver puts body to sleep.

- `sleep_linear_velocity_threshold` (float): [Read-Write] How low the linear velocity can be before solver puts body to sleep.

- `soft_collision_mode` (PhysicalMaterialSoftCollisionMode): [Read-Write] For enable soft collision shell thickness mode

- `soft_collision_thickness` (float): [Read-Write] Thickness of the layer just inside the collision shape in which contact is considered “soft”.

The units depend on SoftCollisionMode

- `static_friction` (float): [Read-Write] Static Friction value of surface, controls how easily things can slide on this surface (0 is frictionless, higher values increase the amount of friction)

- `strength` (PhysicalMaterialStrength): [Read-Write]

- `surface_type` (PhysicalSurface): [Read-Write] To edit surface type for your project, use ProjectSettings/Physics/PhysicalSurface section



---

_property_ `damage_modifier`: PhysicalMaterialDamageModifier

[Read-Only]

**Type:**

( PhysicalMaterialDamageModifier)


---

_property_ `debug_color`: LinearColor

[Read-Only] Color used to represent this material in certain debug views (e.g. landscape collision)

**Type:**

( LinearColor)


---

_property_ `density`: float

[Read-Only] Used with the shape of the object to calculate its mass properties. The higher the number, the heavier the object. g per cubic cm.

**Type:**

( float)


---

_property_ `friction`: float

[Read-Only] Friction value of surface, controls how easily things can slide on this surface (0 is frictionless, higher values increase the amount of friction)

**Type:**

( float)


---

_property_ `friction_combine_mode`: FrictionCombineMode

[Read-Only] Friction combine mode, controls how friction is computed for multiple materials.

**Type:**

( FrictionCombineMode)


---

_property_ `override_friction_combine_mode`: bool

[Read-Write] If set we will use the FrictionCombineMode of this material, instead of the FrictionCombineMode found in the project settings.

**Type:**

( bool)


---

_property_ `override_restitution_combine_mode`: bool

[Read-Write] If set we will use the RestitutionCombineMode of this material, instead of the RestitutionCombineMode found in the project settings.

**Type:**

( bool)


---

_property_ `raise_mass_to_power`: float

[Read-Only] Used to adjust the way that mass increases as objects get larger. This is applied to the mass as calculated based on a ‘solid’ object.
In actuality, larger objects do not tend to be solid, and become more like ‘shells’ (e.g. a car is not a solid piece of metal).
Values are clamped to 1 or less.

**Type:**

( float)


---

_property_ `restitution`: float

[Read-Only] Restitution or ‘bounciness’ of this surface, between 0 (no bounce) and 1 (outgoing velocity is same as incoming).

**Type:**

( float)


---

_property_ `restitution_combine_mode`: FrictionCombineMode

[Read-Only] Restitution combine mode, controls how restitution is computed for multiple materials.

**Type:**

( FrictionCombineMode)


---

_property_ `sleep_angular_velocity_threshold`: float

[Read-Only] How low the angular velocity can be before solver puts body to sleep.

**Type:**

( float)


---

_property_ `sleep_counter_threshold`: int

[Read-Only] How many ticks we can be under thresholds for before solver puts body to sleep.

**Type:**

(int32)


---

_property_ `sleep_linear_velocity_threshold`: float

[Read-Only] How low the linear velocity can be before solver puts body to sleep.

**Type:**

( float)


---

_property_ `static_friction`: float

[Read-Only] Static Friction value of surface, controls how easily things can slide on this surface (0 is frictionless, higher values increase the amount of friction)

**Type:**

( float)


---

_property_ `strength`: PhysicalMaterialStrength

[Read-Only]

**Type:**

( PhysicalMaterialStrength)


---

_property_ `surface_type`: PhysicalSurface

[Read-Only] To edit surface type for your project, use ProjectSettings/Physics/PhysicalSurface section

**Type:**

( PhysicalSurface)

### Table of Contents

- `unreal.PhysicalMaterial`
  - `PhysicalMaterial`
    - `PhysicalMaterial.damage_modifier`
    - `PhysicalMaterial.debug_color`
    - `PhysicalMaterial.density`
    - `PhysicalMaterial.friction`
    - `PhysicalMaterial.friction_combine_mode`
    - `PhysicalMaterial.override_friction_combine_mode`
    - `PhysicalMaterial.override_restitution_combine_mode`
    - `PhysicalMaterial.raise_mass_to_power`
    - `PhysicalMaterial.restitution`
    - `PhysicalMaterial.restitution_combine_mode`
    - `PhysicalMaterial.sleep_angular_velocity_threshold`
    - `PhysicalMaterial.sleep_counter_threshold`
    - `PhysicalMaterial.sleep_linear_velocity_threshold`
    - `PhysicalMaterial.static_friction`
    - `PhysicalMaterial.strength`
    - `PhysicalMaterial.surface_type`