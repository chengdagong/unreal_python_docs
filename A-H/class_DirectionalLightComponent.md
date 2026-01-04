# unreal.DirectionalLightComponent

```python
class unreal.DirectionalLightComponent(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``LightComponent``


A light component that has parallel rays. Will provide a uniform lighting across any affected surface (eg. The Sun). This will affect all objects in the defined light-mass importance volume.

**C++ Source:**

- **Module**: Engine

- **File**: DirectionalLightComponent.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `absolute_location` (bool): [Read-Write] If RelativeLocation should be considered relative to the world, rather than the parent

- `absolute_rotation` (bool): [Read-Write] If RelativeRotation should be considered relative to the world, rather than the parent

- `absolute_scale` (bool): [Read-Write] If RelativeScale3D should be considered relative to the world, rather than the parent

- `affect_global_illumination` (bool): [Read-Write] Whether the light affects global illumination, when ray-traced global illumination is enabled.

- `affect_reflection` (bool): [Read-Write] Whether the light affects objects in reflections, when ray-traced reflection is enabled.

- `affect_translucent_lighting` (bool): [Read-Write] Whether the light affects translucency or not. Disabling this can save GPU time when there are many small lights.

- `affects_world` (bool): [Read-Write] Whether the light can affect the world, or whether it is disabled.
A disabled light will not contribute to the scene in any way. This setting cannot be changed at runtime and unbuilds lighting when changed.
Setting this to false has the same effect as deleting the light, so it is useful for non-destructive experiments.

- `allow_mega_lights` (bool): [Read-Write] Whether to allow this light to use MegaLights, if it is enabled in the project settings or Post Process Volume.
When disabled, the renderer will no longer use stochastic sampling to solve this light’s lighting, and will fall back to other shadowing methods, adding significant GPU cost.

- `asset_user_data` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `asset_user_data_editor_only` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `atmosphere_sun_disk_color_scale` (LinearColor): [Read-Write] A color multiplied with the sun disk luminance.

- `atmosphere_sun_light` (bool): [Read-Write] Whether the directional light can interact with the atmosphere, cloud and generate a visual disk. All of which compose the visual sky.

- `atmosphere_sun_light_index` (int32): [Read-Write] Two atmosphere lights are supported. For instance: a sun and a moon, or two suns.

- `auto_activate` (bool): [Read-Write] Whether the component is activated at creation or must be explicitly activated.

- `bloom_max_brightness` (float): [Read-Write] After exposure is applied, scene color brightness larger than BloomMaxBrightness will be rescaled down to BloomMaxBrightness.

- `bloom_scale` (float): [Read-Write] Scales the additive color.

- `bloom_threshold` (float): [Read-Write] Scene color must be larger than this to create bloom in the light shafts.

- `bloom_tint` (Color): [Read-Write] Multiplies against scene color to create the bloom color.

- `can_ever_affect_navigation` (bool): [Read-Write] Whether this component can potentially influence navigation

- `cascade_distribution_exponent` (float): [Read-Write] Controls whether the cascades are distributed closer to the camera (larger exponent) or further from the camera (smaller exponent).
An exponent of 1 means that cascade transitions will happen at a distance proportional to their resolution.

- `cascade_transition_fraction` (float): [Read-Write] Proportion of the fade region between cascades.
Pixels within the fade region of two cascades have their shadows blended to avoid hard transitions between quality levels.
A value of zero eliminates the fade region, creating hard transitions.
Higher values increase the size of the fade region, creating a more gradual transition between cascades.
The value is expressed as a percentage proportion (i.e. 0.1 = 10% overlap).
Ideal values are the smallest possible which still hide the transition.
An increased fade region size causes an increase in shadow rendering cost.

- `cast_cloud_shadows` (bool): [Read-Write] Whether the light should cast any shadows from clouds onto the atmosphere and other scene elements.

- `cast_deep_shadow` (bool): [Read-Write] Whether the light should cast high quality hair-strands self-shadowing. When this option is enabled, an extra GPU cost for this light.

- `cast_dynamic_shadows` (bool): [Read-Write] Whether the light should cast shadows from dynamic objects. Also requires Cast Shadows to be set to True.

- `cast_modulated_shadows` (bool): [Read-Write] Whether the light should cast modulated shadows from dynamic objects (mobile only). Also requires Cast Shadows to be set to True.

- `cast_raytraced_shadow` (CastRayTracedShadow): [Read-Write]

- `cast_shadows` (bool): [Read-Write] Whether the light should cast any shadows.

- `cast_shadows_from_cinematic_objects_only` (bool): [Read-Write] Whether the light should only cast shadows from components marked as bCastCinematicShadows.
This is useful for setting up cinematic Movable spotlights aimed at characters and avoiding the shadow depth rendering costs of the background.
Note: this only works with dynamic shadow maps, not with static shadowing or Ray Traced Distance Field shadows.

- `cast_shadows_on_atmosphere` (bool): [Read-Write] Whether the light should cast any shadows from opaque meshes onto the atmosphere.

- `cast_shadows_on_clouds` (bool): [Read-Write] Whether the light should cast any shadows from opaque meshes onto clouds. This is disabled when ‘Atmosphere Sun Light Index’ is set to 1.

- `cast_static_shadows` (bool): [Read-Write] Whether the light should cast shadows from static objects. Also requires Cast Shadows to be set to True.

- `cast_translucent_shadows` (bool): [Read-Write] Whether the light is allowed to cast dynamic shadows from translucency.

- `cast_volumetric_shadow` (bool): [Read-Write] Whether the light shadows volumetric fog. Disabling this can save GPU time.

- `cloud_scattered_luminance_scale` (LinearColor): [Read-Write] Scales the lights contribution when scattered in cloud participating media. This can help counter balance the fact that our multiple scattering solution is only an approximation.

- `cloud_shadow_depth_bias` (float): [Read-Write] The bias applied to the shadow front depth of the volumetric cloud shadow map.

- `cloud_shadow_extent` (float): [Read-Write] The world space radius of the cloud shadow map around the camera in kilometers.

- `cloud_shadow_map_resolution_scale` (float): [Read-Write] Scale the cloud shadow map resolution, base resolution is 512. The resolution is still clamped to ‘r.VolumetricCloud.ShadowMap.MaxResolution’.

- `cloud_shadow_on_atmosphere_strength` (float): [Read-Write] The strength of the shadow on atmosphere. Disabled when 0.

- `cloud_shadow_on_surface_strength` (float): [Read-Write] The strength of the shadow on opaque and transparent meshes. Disabled when 0.

- `cloud_shadow_ray_sample_count_scale` (float): [Read-Write] Scale the shadow map tracing sample count.
The sample count resolution is still clamped according to scalability setting to ‘r.VolumetricCloud.ShadowMap.RaySampleMaxCount’.

- `cloud_shadow_strength` (float): [Read-Write] The overall strength of the cloud shadow, higher value will block more light.

- `component_tags` (Array[Name]): [Read-Write] Array of tags that can be used for grouping and categorizing. Can also be accessed from scripting.

- `contact_shadow_casting_intensity` (float): [Read-Write] Intensity of the shadows cast by primitives with “cast contact shadow” enabled. 0 = no shadow, 1 (default) = fully shadowed.

- `contact_shadow_length` (float): [Read-Write] Length of screen space ray trace for sharp contact shadows. Zero is disabled.

- `contact_shadow_length_in_ws` (bool): [Read-Write] Where Length of screen space ray trace for sharp contact shadows is in world space units or in screen space units.

- `contact_shadow_non_casting_intensity` (float): [Read-Write] Intensity of the shadows cast by primitives with “cast contact shadow” disabled. 0 (default) = no shadow, 1 = fully shadowed.

- `deep_shadow_layer_distribution` (float): [Read-Write] Change the deep shadow layers distribution 0:linear distribution (uniform layer distribution), 1:exponential (more details on near small details).

- `detail_mode` (DetailMode): [Read-Write] Set the required detail level of this component.
It will be deleted or made invisible if the world’s detail level is higher, based on platform and scalability settings.
For example, a detail mode of High may prevent this component from loading on mobile platforms.

- `diffuse_scale` (float): [Read-Write] Multiplier on diffuse lighting. Use only with great care! Any value besides 1 is not physical!

- `disabled_brightness` (float): [Read-Write] Brightness factor applied to the light when the light function is specified but disabled, for example in scene captures that use SceneCapView\_LitNoShadows.
This should be set to the average brightness of the light function material’s emissive input, which should be between 0 and 1.

- `distance_field_shadow_distance` (float): [Read-Write] Distance at which the ray traced shadow cascade should end. Distance field shadows will cover the range between ‘Dynamic Shadow Distance’ this distance.

- `dynamic_shadow_cascades` (int32): [Read-Write] Number of cascades to split the view frustum into for the whole scene dynamic shadow.
More cascades result in better shadow resolution, but adds significant rendering cost.

- `dynamic_shadow_distance_movable_light` (float): [Read-Write] How far Cascaded Shadow Map dynamic shadows will cover for a movable light, measured from the camera.
A value of 0 disables the dynamic shadow.

- `dynamic_shadow_distance_stationary_light` (float): [Read-Write] How far Cascaded Shadow Map dynamic shadows will cover for a stationary light, measured from the camera.
A value of 0 disables the dynamic shadow.

- `editable_when_inherited` (bool): [Read-Write] True if this component can be modified when it was inherited from a parent actor class

- `enable_light_shaft_bloom` (bool): [Read-Write] Whether to render light shaft bloom from this light.
For directional lights, the color around the light direction will be blurred radially and added back to the scene.
for point lights, the color on pixels closer than the light’s SourceRadius will be blurred radially and added back to the scene.

- `enable_light_shaft_occlusion` (bool): [Read-Write] Whether to occlude fog and atmosphere inscattering with screenspace blurred occlusion from this light.

- `far_shadow_cascade_count` (int32): [Read-Write] 0: no Far Shadow Cascades, otherwise the number of cascades between DynamicShadowDistance and FarShadowDistance that are covered by Far Shadow Cascades.

- `far_shadow_distance` (float): [Read-Write] Distance at which the far shadow cascade should end. Far shadows will cover the range between ‘Dynamic Shadow Distance’ and this distance.

- `force_cached_shadows_for_movable_primitives` (bool): [Read-Write] Enables cached shadows for movable primitives for this light even if r.shadow.cachedshadowscastfrommovableprimitives is 0

- `forward_shading_priority` (int32): [Read-Write] Forward lighting priority for the single directional light that will be used for forward shading, translucent, single layer water and volumetric fog.
When two lights have equal priorities, the selection will be based on their overall brightness as a fallback.

- `hidden_in_game` (bool): [Read-Write] Whether to hide the primitive in game, if the primitive is Visible.

- `ies_brightness_scale` (float): [Read-Write] Global scale for IES brightness contribution. Only available when “Use IES Brightness” is selected, and a valid IES profile texture is set

- `ies_texture` (TextureLightProfile): [Read-Write] IES texture (light profiles from real world measured data)

- `indirect_lighting_intensity` (float): [Read-Write] Scales the indirect lighting contribution from this light.
A value of 0 disables any GI from this light. Default is 1.

- `intensity` (float): [Read-Write] Total energy that the light emits.

- `is_editor_only` (bool): [Read-Write] If true, the component will be excluded from non-editor builds

- `light_color` (Color): [Read-Write] Filter color of the light.
Note that this can change the light’s effective intensity.

- `light_function_fade_distance` (float): [Read-Write] Distance at which the light function should be completely faded to DisabledBrightness.
This is useful for hiding aliasing from light functions applied in the distance.

- `light_function_material` (MaterialInterface): [Read-Write] The light function material to be applied to this light.
Note that only non-lightmapped lights (UseDirectLightMap=False) can have a light function.
Light functions are supported within VolumetricFog, but only for Directional, Point and Spot lights. Rect lights are not supported.

- `light_function_scale` (Vector): [Read-Write] Scales the light function projection. X and Y scale in the directions perpendicular to the light’s direction, Z scales along the light direction.

- `light_shaft_override_direction` (Vector): [Read-Write] Can be used to make light shafts come from somewhere other than the light’s actual direction.
This will only be used when non-zero. It does not have to be normalized.

- `light_source_angle` (float): [Read-Write] Angle subtended by light source in degrees (also known as angular diameter).
Defaults to 0.5357 which is the angle for our sun.

- `light_source_soft_angle` (float): [Read-Write] Angle subtended by soft light source in degrees.

- `lighting_channels` (LightingChannels): [Read-Write] Channels that this light should affect.
These channels only apply to opaque materials, direct lighting, and dynamic lighting and shadowing.
Lighting channels are only supported on translucent materials using forward shading (i.e. when not using the translucency lighting volume).

- `lightmass_settings` (LightmassDirectionalLightSettings): [Read-Write] The Lightmass settings for this object.

- `max_distance_fade_range` (float): [Read-Write] Fade the light out as it approaches MaxDrawDistance. The fading starts when the light is MaxDistanceFadeRange distance away from MaxDrawDistance, where it ends up at 0 for a smooth fade-out without popping. Requires MaxDrawDistance to be set.

- `max_draw_distance` (float): [Read-Write] World distance to where the light stops rendering (lighting & shadows). 0.0 or less means no max draw distance. This can be controlled via a global scalar scalability setting r.LightMaxDrawDistanceScale as well

- `mega_lights_shadow_method` (MegaLightsShadowMethod): [Read-Write] Selects which shadowing method should MegaLights use for this light.
RayTracing - Preferred method, which guarantees fixed MegaLights cost and correct area shadows, but is dependent on the BVH representation quality.
VirtualShadowMap - Has a significant per light cost, but can cast shadows directly from the Nanite geometry using rasterization.

- `mobility` (ComponentMobility): [Read-Write] How often this component is allowed to move, used to make various optimizations. Only safe to set in constructor.

- `modulated_shadow_color` (Color): [Read-Write] Color to modulate against the scene color when rendering modulated shadows. (mobile only)

- `occlusion_depth_range` (float): [Read-Write] Everything closer to the camera than this distance will occlude light shafts.

- `occlusion_mask_darkness` (float): [Read-Write] Controls how dark the occlusion masking is, a value of 1 results in no darkening term.

- `on_component_activated` (ActorComponentActivatedSignature): [Read-Write] Called when the component has been activated, with parameter indicating if it was from a reset

- `on_component_deactivated` (ActorComponentDeactivateSignature): [Read-Write] Called when the component has been deactivated

- `override_ray_end_bias` (bool): [Read-Write]

- `per_pixel_atmosphere_transmittance` (bool): [Read-Write] Whether to apply atmosphere transmittance per pixel on opaque meshes, instead of using the light global transmittance. Note: VolumetricCloud per pixel transmittance option is selectable on the VolumetricCloud component itself.

- `physics_volume_changed_delegate` (PhysicsVolumeChanged): [Read-Write] Delegate that will be called when PhysicsVolume has been changed \*

- `primary_component_tick` (ActorComponentTickFunction): [Read-Write] Main tick function for the Component

- `ray_end_bias` (float): [Read-Write]

- `ray_start_offset_depth_scale` (float): [Read-Write] Controls how large of an offset ray traced shadows have from the receiving surface as the camera gets further away.
This can be useful to hide self-shadowing artifacts from low resolution distance fields on huge static meshes.

- `relative_location` (Vector): [Read-Write] Location of the component relative to its parent

- `relative_rotation` (Rotator): [Read-Write] Rotation of the component relative to its parent

- `relative_scale3d` (Vector): [Read-Write] Non-uniform scaling of the component relative to its parent.
Note that scaling is always applied in local space (no shearing etc)

- `replicate_using_registered_sub_object_list` (bool): [Read-Write] When true the replication system will only replicate the registered subobjects list
When false the replication system will instead call the virtual ReplicateSubObjects() function where the subobjects need to be manually replicated.

- `replicates` (bool): [Read-Write] Is this component currently replicating? Should the network code consider it for replication? Owning Actor must be replicating first!

- `samples_per_pixel` (int32): [Read-Write] Samples per pixel for ray tracing

- `shadow_amount` (float): [Read-Write] Control the amount of shadow occlusion. A value of 0 means no occlusion, thus no shadow.

- `shadow_bias` (float): [Read-Write] Controls how accurate self shadowing of whole scene shadows from this light are.
At 0, shadows will start at the their caster surface, but there will be many self shadowing artifacts.
larger values, shadows will start further from their caster, and there won’t be self shadowing artifacts but object might appear to fly.
around 0.5 seems to be a good tradeoff. This also affects the soft transition of shadows

- `shadow_cascade_bias_distribution` (float): [Read-Write] Controls the depth bias scaling across cascades. This allows to mitigage the shadow acne difference on shadow cascades transition.
A value of 1 scales shadow bias based on each cascade size (Default).
A value of 0 scales shadow bias uniformly accross all cacascade.

- `shadow_distance_fadeout_fraction` (float): [Read-Write] Controls the size of the fade out region at the far extent of the dynamic shadow’s influence.
This is specified as a fraction of DynamicShadowDistance.

- `shadow_resolution_scale` (float): [Read-Write] Scales the resolution of shadowmaps used to shadow this light. By default shadowmap resolution is chosen based on screen size of the caster.
Setting the scale to zero disables shadow maps, but does not disable, e.g., contact shadows.
Note: shadowmap resolution is still clamped by ‘r.Shadow.MaxResolution’

- `shadow_sharpen` (float): [Read-Write] Amount to sharpen shadow filtering

- `shadow_slope_bias` (float): [Read-Write] Controls how accurate self shadowing of whole scene shadows from this light are. This works in addition to shadow bias, by increasing the
amount of bias depending on the slope of a surface.
At 0, shadows will start at the their caster surface, but there will be many self shadowing artifacts.
larger values, shadows will start further from their caster, and there won’t be self shadowing artifacts but object might appear to fly.
around 0.5 seems to be a good tradeoff. This also affects the soft transition of shadows

- `shadow_source_angle_factor` (float): [Read-Write] Shadow source angle factor, relative to the light source angle.
Defaults to 1.0 to coincide with light source angle.

- `should_update_physics_volume` (bool): [Read-Write] Whether or not the cached PhysicsVolume this component overlaps should be updated when the component is moved.
see: GetPhysicsVolume()

- `specular_scale` (float): [Read-Write] Multiplier on specular highlights. Use only with great care! Any value besides 1 is not physical!
Can be used to artistically remove highlights mimicking polarizing filters or photo touch up.

- `temperature` (float): [Read-Write] Color temperature in Kelvin of the blackbody illuminant.
White (D65) is 6500K.

- `trace_distance` (float): [Read-Write] Determines how far shadows can be cast, in world units. Larger values increase the shadowing cost.

- `transmission` (bool): [Read-Write] Whether light from this light transmits through surfaces with subsurface scattering profiles. Requires light to be movable.

- `use_attach_parent_bound` (bool): [Read-Write] If true, this component uses its parents bounds when attached.
This can be a significant optimization with many components attached together.

- `use_ies_brightness` (bool): [Read-Write] true: take light brightness from IES profile, false: use the light brightness - the maximum light in one direction is used to define no masking. Use with InverseSquareFalloff. Will be disabled if a valid IES profile texture is not supplied.

- `use_inset_shadows_for_movable_objects` (bool): [Read-Write] Stationary lights only: Whether to use per-object inset shadows for movable components, even though cascaded shadow maps are enabled.
This allows dynamic objects to have a shadow even when they are outside of the cascaded shadow map, which is important when DynamicShadowDistanceStationaryLight is small.
If DynamicShadowDistanceStationaryLight is large (currently > 8000), this will be forced off.
Disabling this can reduce shadowing cost significantly with many movable objects.

- `use_ray_traced_distance_field_shadows` (bool): [Read-Write] Whether to use ray traced distance field area shadows. The project setting bGenerateMeshDistanceFields must be enabled for this to have effect.
Distance field shadows support area lights so they create soft shadows with sharp contacts.
They have less aliasing artifacts than standard shadowmaps, but inherit all the limitations of distance field representations (only uniform scale, no deformation).
These shadows have a low per-object cost (and don’t depend on triangle count) so they are effective for distant shadows from a dynamic sun.

- `use_temperature` (bool): [Read-Write] false: use white (D65) as illuminant.

- `view_lighting_channels` (ViewLightingChannels): [Read-Write] View / light masking support. Controls which views this light should affect.

- `visible` (bool): [Read-Write] Whether to completely draw the primitive; if false, the primitive is not drawn, does not cast a shadow.

- `volumetric_scattering_intensity` (float): [Read-Write] Intensity of the volumetric scattering from this light. This scales Intensity and LightColor.



---

_property_ `atmosphere_sun_disk_color_scale`: LinearColor

[Read-Only] A color multiplied with the sun disk luminance.

**Type:**

( LinearColor)


---

_property_ `atmosphere_sun_light`: bool

[Read-Only] Whether the directional light can interact with the atmosphere, cloud and generate a visual disk. All of which compose the visual sky.

**Type:**

( bool)


---

_property_ `atmosphere_sun_light_index`: int

a sun and a moon, or two suns.

**Type:**

(int32)

**Type:**

[Read-Only] Two atmosphere lights are supported. For instance


---

_property_ `cascade_distribution_exponent`: float

[Read-Only] Controls whether the cascades are distributed closer to the camera (larger exponent) or further from the camera (smaller exponent).
An exponent of 1 means that cascade transitions will happen at a distance proportional to their resolution.

**Type:**

( float)


---

_property_ `cascade_transition_fraction`: float

[Read-Only] Proportion of the fade region between cascades.
Pixels within the fade region of two cascades have their shadows blended to avoid hard transitions between quality levels.
A value of zero eliminates the fade region, creating hard transitions.
Higher values increase the size of the fade region, creating a more gradual transition between cascades.
The value is expressed as a percentage proportion (i.e. 0.1 = 10% overlap).
Ideal values are the smallest possible which still hide the transition.
An increased fade region size causes an increase in shadow rendering cost.

**Type:**

( float)


---

_property_ `cast_cloud_shadows`: bool

[Read-Only] Whether the light should cast any shadows from clouds onto the atmosphere and other scene elements.

**Type:**

( bool)


---

_property_ `cast_modulated_shadows`: bool

[Read-Only] Whether the light should cast modulated shadows from dynamic objects (mobile only). Also requires Cast Shadows to be set to True.

**Type:**

( bool)


---

_property_ `cast_shadows_on_atmosphere`: bool

[Read-Only] Whether the light should cast any shadows from opaque meshes onto the atmosphere.

**Type:**

( bool)


---

_property_ `cast_shadows_on_clouds`: bool

[Read-Only] Whether the light should cast any shadows from opaque meshes onto clouds. This is disabled when ‘Atmosphere Sun Light Index’ is set to 1.

**Type:**

( bool)


---

_property_ `cloud_scattered_luminance_scale`: LinearColor

[Read-Only] Scales the lights contribution when scattered in cloud participating media. This can help counter balance the fact that our multiple scattering solution is only an approximation.

**Type:**

( LinearColor)


---

_property_ `cloud_shadow_depth_bias`: float

[Read-Only] The bias applied to the shadow front depth of the volumetric cloud shadow map.

**Type:**

( float)


---

_property_ `cloud_shadow_extent`: float

[Read-Only] The world space radius of the cloud shadow map around the camera in kilometers.

**Type:**

( float)


---

_property_ `cloud_shadow_map_resolution_scale`: float

[Read-Only] Scale the cloud shadow map resolution, base resolution is 512. The resolution is still clamped to ‘r.VolumetricCloud.ShadowMap.MaxResolution’.

**Type:**

( float)


---

_property_ `cloud_shadow_on_atmosphere_strength`: float

[Read-Only] The strength of the shadow on atmosphere. Disabled when 0.

**Type:**

( float)


---

_property_ `cloud_shadow_on_surface_strength`: float

[Read-Only] The strength of the shadow on opaque and transparent meshes. Disabled when 0.

**Type:**

( float)


---

_property_ `cloud_shadow_ray_sample_count_scale`: float

[Read-Only] Scale the shadow map tracing sample count.
The sample count resolution is still clamped according to scalability setting to ‘r.VolumetricCloud.ShadowMap.RaySampleMaxCount’.

**Type:**

( float)


---

_property_ `cloud_shadow_strength`: float

[Read-Only] The overall strength of the cloud shadow, higher value will block more light.

**Type:**

( float)


---

_property_ `distance_field_shadow_distance`: float

[Read-Only] Distance at which the ray traced shadow cascade should end. Distance field shadows will cover the range between ‘Dynamic Shadow Distance’ this distance.

**Type:**

( float)


---

_property_ `dynamic_shadow_cascades`: int

[Read-Only] Number of cascades to split the view frustum into for the whole scene dynamic shadow.
More cascades result in better shadow resolution, but adds significant rendering cost.

**Type:**

(int32)


---

_property_ `dynamic_shadow_distance_movable_light`: float

[Read-Only] How far Cascaded Shadow Map dynamic shadows will cover for a movable light, measured from the camera.
A value of 0 disables the dynamic shadow.

**Type:**

( float)


---

_property_ `dynamic_shadow_distance_stationary_light`: float

[Read-Only] How far Cascaded Shadow Map dynamic shadows will cover for a stationary light, measured from the camera.
A value of 0 disables the dynamic shadow.

**Type:**

( float)


---

_property_ `enable_light_shaft_occlusion`: bool

[Read-Only] Whether to occlude fog and atmosphere inscattering with screenspace blurred occlusion from this light.

**Type:**

( bool)


---

_property_ `far_shadow_cascade_count`: int

no Far Shadow Cascades, otherwise the number of cascades between DynamicShadowDistance and FarShadowDistance that are covered by Far Shadow Cascades.

**Type:**

(int32)

**Type:**

[Read-Only] 0


---

_property_ `far_shadow_distance`: float

[Read-Only] Distance at which the far shadow cascade should end. Far shadows will cover the range between ‘Dynamic Shadow Distance’ and this distance.

**Type:**

( float)


---

_property_ `forward_shading_priority`: int

[Read-Only] Forward lighting priority for the single directional light that will be used for forward shading, translucent, single layer water and volumetric fog.
When two lights have equal priorities, the selection will be based on their overall brightness as a fallback.

**Type:**

(int32)


---

_property_ `light_shaft_override_direction`: Vector

[Read-Only] Can be used to make light shafts come from somewhere other than the light’s actual direction.
This will only be used when non-zero. It does not have to be normalized.

**Type:**

( Vector)


---

_property_ `light_source_angle`: float

[Read-Only] Angle subtended by light source in degrees (also known as angular diameter).
Defaults to 0.5357 which is the angle for our sun.

**Type:**

( float)


---

_property_ `light_source_soft_angle`: float

[Read-Only] Angle subtended by soft light source in degrees.

**Type:**

( float)


---

_property_ `modulated_shadow_color`: Color

[Read-Only] Color to modulate against the scene color when rendering modulated shadows. (mobile only)

**Type:**

( Color)


---

_property_ `movable_whole_scene_dynamic_shadow_radius`: float

‘movable\_whole\_scene\_dynamic\_shadow\_radius’ was renamed to ‘dynamic\_shadow\_distance\_movable\_light’.

**Type:**

deprecated


---

_property_ `occlusion_depth_range`: float

[Read-Only] Everything closer to the camera than this distance will occlude light shafts.

**Type:**

( float)


---

_property_ `occlusion_mask_darkness`: float

[Read-Only] Controls how dark the occlusion masking is, a value of 1 results in no darkening term.

**Type:**

( float)


---

_property_ `per_pixel_atmosphere_transmittance`: bool

VolumetricCloud per pixel transmittance option is selectable on the VolumetricCloud component itself.

**Type:**

( bool)

**Type:**

[Read-Only] Whether to apply atmosphere transmittance per pixel on opaque meshes, instead of using the light global transmittance. Note


---

**set_atmosphere_sun_disk_color_scale**( _new_value_) → `None`

Set Atmosphere Sun Disk Color Scale

Parameters:

**new\_value** ( _LinearColor_)


---

**set_atmosphere_sun_light**( _new_value_) → `None`

Set Atmosphere Sun Light

Parameters:

**new\_value** ( _bool_)


---

**set_atmosphere_sun_light_index**( _new_value_) → `None`

Set Atmosphere Sun Light Index

Parameters:

**new\_value** ( _int32_)


---

**set_cascade_distribution_exponent**( _new_value_) → `None`

Set Cascade Distribution Exponent

Parameters:

**new\_value** ( _float_)


---

**set_cascade_transition_fraction**( _new_value_) → `None`

Set Cascade Transition Fraction

Parameters:

**new\_value** ( _float_)


---

**set_dynamic_shadow_cascades**( _new_value_) → `None`

Set Dynamic Shadow Cascades

Parameters:

**new\_value** ( _int32_)


---

**set_dynamic_shadow_distance_movable_light**( _new_value_) → `None`

Set Dynamic Shadow Distance Movable Light

Parameters:

**new\_value** ( _float_)


---

**set_dynamic_shadow_distance_stationary_light**( _new_value_) → `None`

Set Dynamic Shadow Distance Stationary Light

Parameters:

**new\_value** ( _float_)


---

**set_enable_light_shaft_occlusion**( _new_value_) → `None`

Set Enable Light Shaft Occlusion

Parameters:

**new\_value** ( _bool_)


---

**set_forward_shading_priority**( _new_value_) → `None`

Set Forward Shading Priority

Parameters:

**new\_value** ( _int32_)


---

**set_light_shaft_override_direction**( _new_value_) → `None`

Set Light Shaft Override Direction

Parameters:

**new\_value** ( _Vector_)


---

**set_light_source_angle**( _new_value_) → `None`

Set Light Source Angle

Parameters:

**new\_value** ( _float_)


---

**set_light_source_soft_angle**( _new_value_) → `None`

Set Light Source Soft Angle

Parameters:

**new\_value** ( _float_)


---

**set_occlusion_depth_range**( _new_value_) → `None`

Set Occlusion Depth Range

Parameters:

**new\_value** ( _float_)


---

**set_occlusion_mask_darkness**( _new_value_) → `None`

Set Occlusion Mask Darkness

Parameters:

**new\_value** ( _float_)


---

**set_shadow_amount**( _new_value_) → `None`

Set Shadow Amount

Parameters:

**new\_value** ( _float_)


---

**set_shadow_cascade_bias_distribution**( _new_value_) → `None`

Set Shadow Cascade Bias Distribution

Parameters:

**new\_value** ( _float_)


---

**set_shadow_distance_fadeout_fraction**( _new_value_) → `None`

Set Shadow Distance Fadeout Fraction

Parameters:

**new\_value** ( _float_)


---

**set_shadow_source_angle_factor**( _new_value_) → `None`

Set Shadow Source Angle Factor

Parameters:

**new\_value** ( _float_)


---

_property_ `shadow_amount`: float

[Read-Only] Control the amount of shadow occlusion. A value of 0 means no occlusion, thus no shadow.

**Type:**

( float)


---

_property_ `shadow_cascade_bias_distribution`: float

[Read-Only] Controls the depth bias scaling across cascades. This allows to mitigage the shadow acne difference on shadow cascades transition.
A value of 1 scales shadow bias based on each cascade size (Default).
A value of 0 scales shadow bias uniformly accross all cacascade.

**Type:**

( float)


---

_property_ `shadow_distance_fadeout_fraction`: float

[Read-Only] Controls the size of the fade out region at the far extent of the dynamic shadow’s influence.
This is specified as a fraction of DynamicShadowDistance.

**Type:**

( float)


---

_property_ `shadow_source_angle_factor`: float

[Read-Only] Shadow source angle factor, relative to the light source angle.
Defaults to 1.0 to coincide with light source angle.

**Type:**

( float)


---

_property_ `stationary_whole_scene_dynamic_shadow_radius`: float

‘stationary\_whole\_scene\_dynamic\_shadow\_radius’ was renamed to ‘dynamic\_shadow\_distance\_stationary\_light’.

**Type:**

deprecated


---

_property_ `trace_distance`: float

[Read-Only] Determines how far shadows can be cast, in world units. Larger values increase the shadowing cost.

**Type:**

( float)


---

_property_ `use_inset_shadows_for_movable_objects`: bool

Whether to use per-object inset shadows for movable components, even though cascaded shadow maps are enabled.
This allows dynamic objects to have a shadow even when they are outside of the cascaded shadow map, which is important when DynamicShadowDistanceStationaryLight is small.
If DynamicShadowDistanceStationaryLight is large (currently > 8000), this will be forced off.
Disabling this can reduce shadowing cost significantly with many movable objects.

**Type:**

( bool)

**Type:**

[Read-Only] Stationary lights only

### Table of Contents

- `unreal.DirectionalLightComponent`
  - `DirectionalLightComponent`
    - `DirectionalLightComponent.atmosphere_sun_disk_color_scale`
    - `DirectionalLightComponent.atmosphere_sun_light`
    - `DirectionalLightComponent.atmosphere_sun_light_index`
    - `DirectionalLightComponent.cascade_distribution_exponent`
    - `DirectionalLightComponent.cascade_transition_fraction`
    - `DirectionalLightComponent.cast_cloud_shadows`
    - `DirectionalLightComponent.cast_modulated_shadows`
    - `DirectionalLightComponent.cast_shadows_on_atmosphere`
    - `DirectionalLightComponent.cast_shadows_on_clouds`
    - `DirectionalLightComponent.cloud_scattered_luminance_scale`
    - `DirectionalLightComponent.cloud_shadow_depth_bias`
    - `DirectionalLightComponent.cloud_shadow_extent`
    - `DirectionalLightComponent.cloud_shadow_map_resolution_scale`
    - `DirectionalLightComponent.cloud_shadow_on_atmosphere_strength`
    - `DirectionalLightComponent.cloud_shadow_on_surface_strength`
    - `DirectionalLightComponent.cloud_shadow_ray_sample_count_scale`
    - `DirectionalLightComponent.cloud_shadow_strength`
    - `DirectionalLightComponent.distance_field_shadow_distance`
    - `DirectionalLightComponent.dynamic_shadow_cascades`
    - `DirectionalLightComponent.dynamic_shadow_distance_movable_light`
    - `DirectionalLightComponent.dynamic_shadow_distance_stationary_light`
    - `DirectionalLightComponent.enable_light_shaft_occlusion`
    - `DirectionalLightComponent.far_shadow_cascade_count`
    - `DirectionalLightComponent.far_shadow_distance`
    - `DirectionalLightComponent.forward_shading_priority`
    - `DirectionalLightComponent.light_shaft_override_direction`
    - `DirectionalLightComponent.light_source_angle`
    - `DirectionalLightComponent.light_source_soft_angle`
    - `DirectionalLightComponent.modulated_shadow_color`
    - `DirectionalLightComponent.movable_whole_scene_dynamic_shadow_radius`
    - `DirectionalLightComponent.occlusion_depth_range`
    - `DirectionalLightComponent.occlusion_mask_darkness`
    - `DirectionalLightComponent.per_pixel_atmosphere_transmittance`
    - `DirectionalLightComponent.set_atmosphere_sun_disk_color_scale()`
    - `DirectionalLightComponent.set_atmosphere_sun_light()`
    - `DirectionalLightComponent.set_atmosphere_sun_light_index()`
    - `DirectionalLightComponent.set_cascade_distribution_exponent()`
    - `DirectionalLightComponent.set_cascade_transition_fraction()`
    - `DirectionalLightComponent.set_dynamic_shadow_cascades()`
    - `DirectionalLightComponent.set_dynamic_shadow_distance_movable_light()`
    - `DirectionalLightComponent.set_dynamic_shadow_distance_stationary_light()`
    - `DirectionalLightComponent.set_enable_light_shaft_occlusion()`
    - `DirectionalLightComponent.set_forward_shading_priority()`
    - `DirectionalLightComponent.set_light_shaft_override_direction()`
    - `DirectionalLightComponent.set_light_source_angle()`
    - `DirectionalLightComponent.set_light_source_soft_angle()`
    - `DirectionalLightComponent.set_occlusion_depth_range()`
    - `DirectionalLightComponent.set_occlusion_mask_darkness()`
    - `DirectionalLightComponent.set_shadow_amount()`
    - `DirectionalLightComponent.set_shadow_cascade_bias_distribution()`
    - `DirectionalLightComponent.set_shadow_distance_fadeout_fraction()`
    - `DirectionalLightComponent.set_shadow_source_angle_factor()`
    - `DirectionalLightComponent.shadow_amount`
    - `DirectionalLightComponent.shadow_cascade_bias_distribution`
    - `DirectionalLightComponent.shadow_distance_fadeout_fraction`
    - `DirectionalLightComponent.shadow_source_angle_factor`
    - `DirectionalLightComponent.stationary_whole_scene_dynamic_shadow_radius`
    - `DirectionalLightComponent.trace_distance`
    - `DirectionalLightComponent.use_inset_shadows_for_movable_objects`