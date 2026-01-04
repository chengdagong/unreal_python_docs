# unreal.NiagaraSimCacheCreateParameters

```python
class unreal.NiagaraSimCacheCreateParameters(attribute_capture_mode:NiagaraSimCacheAttributeCaptureMode=Ellipsis, allow_rebasing:bool=False, allow_data_interface_caching:bool=False, allow_interpolation:bool=False, interpolate_all_types:bool=False, allow_velocity_extrapolation:bool=False, allow_serialize_large_cache:bool=False, include_debug_data:bool=False, rebase_include_attributes:None=\[\], rebase_exclude_attributes:None=\[\], interpolation_include_attributes:None=\[\], interpolation_exclude_attributes:None=\[\], explicit_capture_attributes:None=\[\])
```


**Bases:** ``StructBase``


Niagara Sim Cache Create Parameters

**C++ Source:**

- **Plugin**: Niagara

- **Module**: Niagara

- **File**: NiagaraSimCache.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `allow_data_interface_caching` (bool): [Read-Write] When enabled Data Interface data will be stored in the SimCache.
This can result in a large increase to the cache size, depending on what Data Interfaces are used

- `allow_interpolation` (bool): [Read-Write] When enabled we allow the cache to be generated for interpolation.
This will increase the memory usage for the cache slightly but can allow you to reduce the capture rate.

- `allow_rebasing` (bool): [Read-Write] When enabled allows the SimCache to be re-based.
i.e. World space emitters can be moved to the new component’s location

- `allow_serialize_large_cache` (bool): [Read-Write] When enabled the cache will support serializing large amounts of cache data.

- `allow_velocity_extrapolation` (bool): [Read-Write] When enabled we allow the cache to be generated for extrapolation.
This will force the velocity attribute to be maintained.

- `attribute_capture_mode` (NiagaraSimCacheAttributeCaptureMode): [Read-Write] How do we want to capture attributes for the simulation cache.
The mode selected depends on what situations the cache can be used in.

- `explicit_capture_attributes` (Array[Name]): [Read-Write] List of attributes to capture when the capture attribute capture mode is set to explicit.
For example, adding MyEmitter.Particles.Position will only gather that attribute inside the cache.

- `include_debug_data` (bool): [Read-Write] When enabled additional information is stored that can be useful for debugging a simulation

- `interpolate_all_types` (bool): [Read-Write] When enabled all support types for interpolation will be included, this set may increase in future releases.
When disabled we only interpolate Position / Quat attributes.

- `interpolation_exclude_attributes` (Array[Name]): [Read-Write] List of specific Attributes to exclude interpolation for. They must be types that are supported for interpolation.
For example, MyEmitter.Particles.MyPosition would force MyPosition to be interpolated.

- `interpolation_include_attributes` (Array[Name]): [Read-Write] List of specific Attributes to include when using interpolation. They must be types that are supported for interpolation.
For example, MyEmitter.Particles.MyPosition would force MyPosition to be interpolated.

- `rebase_exclude_attributes` (Array[Name]): [Read-Write] List of Attributes to force exclude from the SimCache rebase, they should be the full path to the attribute
For example, MyEmitter.Particles.MyQuat would force the particle attribute MyQuat to be included for MyEmitter

- `rebase_include_attributes` (Array[Name]): [Read-Write] List of Attributes to force include in the SimCache rebase, they should be the full path to the attribute
For example, MyEmitter.Particles.MyQuat would force the particle attribute MyQuat to be included for MyEmitter



---

_property_ `allow_data_interface_caching`: bool

[Read-Write] When enabled Data Interface data will be stored in the SimCache.
This can result in a large increase to the cache size, depending on what Data Interfaces are used

**Type:**

( bool)


---

_property_ `allow_interpolation`: bool

[Read-Write] When enabled we allow the cache to be generated for interpolation.
This will increase the memory usage for the cache slightly but can allow you to reduce the capture rate.

**Type:**

( bool)


---

_property_ `allow_rebasing`: bool

[Read-Write] When enabled allows the SimCache to be re-based.
i.e. World space emitters can be moved to the new component’s location

**Type:**

( bool)


---

_property_ `allow_serialize_large_cache`: bool

[Read-Write] When enabled the cache will support serializing large amounts of cache data.

**Type:**

( bool)


---

_property_ `allow_velocity_extrapolation`: bool

[Read-Write] When enabled we allow the cache to be generated for extrapolation.
This will force the velocity attribute to be maintained.

**Type:**

( bool)


---

_property_ `attribute_capture_mode`: NiagaraSimCacheAttributeCaptureMode

[Read-Write] How do we want to capture attributes for the simulation cache.
The mode selected depends on what situations the cache can be used in.

**Type:**

( NiagaraSimCacheAttributeCaptureMode)


---

_property_ `explicit_capture_attributes`: None

[Read-Write] List of attributes to capture when the capture attribute capture mode is set to explicit.
For example, adding MyEmitter.Particles.Position will only gather that attribute inside the cache.

**Type:**

( Array\ [Name])


---

_property_ `include_debug_data`: bool

[Read-Write] When enabled additional information is stored that can be useful for debugging a simulation

**Type:**

( bool)


---

_property_ `interpolate_all_types`: bool

[Read-Write] When enabled all support types for interpolation will be included, this set may increase in future releases.
When disabled we only interpolate Position / Quat attributes.

**Type:**

( bool)


---

_property_ `interpolation_exclude_attributes`: None

[Read-Write] List of specific Attributes to exclude interpolation for. They must be types that are supported for interpolation.
For example, MyEmitter.Particles.MyPosition would force MyPosition to be interpolated.

**Type:**

( Array\ [Name])


---

_property_ `interpolation_include_attributes`: None

[Read-Write] List of specific Attributes to include when using interpolation. They must be types that are supported for interpolation.
For example, MyEmitter.Particles.MyPosition would force MyPosition to be interpolated.

**Type:**

( Array\ [Name])


---

_property_ `rebase_exclude_attributes`: None

[Read-Write] List of Attributes to force exclude from the SimCache rebase, they should be the full path to the attribute
For example, MyEmitter.Particles.MyQuat would force the particle attribute MyQuat to be included for MyEmitter

**Type:**

( Array\ [Name])


---

_property_ `rebase_include_attributes`: None

[Read-Write] List of Attributes to force include in the SimCache rebase, they should be the full path to the attribute
For example, MyEmitter.Particles.MyQuat would force the particle attribute MyQuat to be included for MyEmitter

**Type:**

( Array\ [Name])

### Table of Contents

- `unreal.NiagaraSimCacheCreateParameters`
  - `NiagaraSimCacheCreateParameters`
    - `NiagaraSimCacheCreateParameters.allow_data_interface_caching`
    - `NiagaraSimCacheCreateParameters.allow_interpolation`
    - `NiagaraSimCacheCreateParameters.allow_rebasing`
    - `NiagaraSimCacheCreateParameters.allow_serialize_large_cache`
    - `NiagaraSimCacheCreateParameters.allow_velocity_extrapolation`
    - `NiagaraSimCacheCreateParameters.attribute_capture_mode`
    - `NiagaraSimCacheCreateParameters.explicit_capture_attributes`
    - `NiagaraSimCacheCreateParameters.include_debug_data`
    - `NiagaraSimCacheCreateParameters.interpolate_all_types`
    - `NiagaraSimCacheCreateParameters.interpolation_exclude_attributes`
    - `NiagaraSimCacheCreateParameters.interpolation_include_attributes`
    - `NiagaraSimCacheCreateParameters.rebase_exclude_attributes`
    - `NiagaraSimCacheCreateParameters.rebase_include_attributes`