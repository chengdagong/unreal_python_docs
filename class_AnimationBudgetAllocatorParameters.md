# unreal.AnimationBudgetAllocatorParameters

```python
class unreal.AnimationBudgetAllocatorParameters(budget_in_ms:float=0.0, min_quality:float=0.0, max_tick_rate:int=0, work_unit_smoothing_speed:float=0.0, always_tick_falloff_aggression:float=0.0, interpolation_falloff_aggression:float=0.0, interpolation_max_rate:int=0, max_interpolated_components:int=0, interpolation_tick_multiplier:float=0.0, initial_estimated_work_unit_time_ms:float=0.0, max_ticked_offsreen_components:int=0, state_change_throttle_in_frames:int=0, budget_factor_before_reduced_work:float=0.0, budget_factor_before_reduced_work_epsilon:float=0.0, budget_pressure_smoothing_speed:float=0.0, reduced_work_throttle_min_in_frames:int=0, reduced_work_throttle_max_in_frames:int=0, budget_factor_before_aggressive_reduced_work:float=0.0, reduced_work_throttle_max_per_frame:int=0, budget_pressure_before_emergency_reduced_work:float=0.0, auto_calculated_significance_max_distance:float=0.0)
```


**Bases:** ``StructBase``


Parameter block used to control the behavior of the budget allocator

**C++ Source:**

- **Plugin**: AnimationBudgetAllocator

- **Module**: AnimationBudgetAllocator

- **File**: AnimationBudgetAllocatorParameters.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `always_tick_falloff_aggression` (float): [Read-Write] Range [0.1, 0.9].
Controls the rate at which ‘always ticked’ components falloff under load.
Higher values mean that we reduce the number of always ticking components by a larger amount when the allocated time budget is exceeded.

- `auto_calculated_significance_max_distance` (float): [Read-Write] Range > 1.0.
Controls the distance at which auto-calculated significance for budgeted components bottoms out. Components
within the distance 1 -> Max will have significance mapped 1 -> 0, outside of MaxDistance significance will be zero.

- `budget_factor_before_aggressive_reduced_work` (float): [Read-Write] Range > 1.
Reduced work will be applied more rapidly when budget pressure goes over this amount.

- `budget_factor_before_reduced_work` (float): [Read-Write] Range > 1
Reduced work will be delayed until budget pressure goes over this amount.

- `budget_factor_before_reduced_work_epsilon` (float): [Read-Write] Range > 0.0.
Increased work will be delayed until budget pressure goes under BudgetFactorBeforeReducedWork minus this amount.

- `budget_in_ms` (float): [Read-Write] Values > 0.1.
The time in milliseconds that we allocate for skeletal mesh work to be performed.
When overbudget various other parameters come into play, such as AlwaysTickFalloffAggression and InterpolationFalloffAggression.

- `budget_pressure_before_emergency_reduced_work` (float): [Read-Write] Range > 0.0.
Controls the budget pressure where emergency reduced work (applied to all components except those that are bAlwaysTick).

- `budget_pressure_smoothing_speed` (float): [Read-Write] Range > 0.0.
How much to smooth the budget pressure value used to throttle reduced work.

- `initial_estimated_work_unit_time_ms` (float): [Read-Write] Values > 0.0.
Controls the time in milliseconds we expect, on average, for a skeletal mesh component to execute.
The value only applies for the first tick of a component, after which we use the real time the tick takes.

- `interpolation_falloff_aggression` (float): [Read-Write] Range [0.1, 0.9].
Controls the rate at which interpolated components falloff under load.
Higher values mean that we reduce the number of interpolated components by a larger amount when the allocated time budget is exceeded.
Components are only interpolated when the time budget is exceeded.

- `interpolation_max_rate` (int32): [Read-Write] Values > 1.
Controls the rate at which ticks happen when interpolating.

- `interpolation_tick_multiplier` (float): [Read-Write] Range [0.1, 0.9].
Controls the expected value an amortized interpolated tick will take compared to a ‘normal’ tick.

- `max_interpolated_components` (int32): [Read-Write] Range >= 0.
Max number of components to interpolate before we start throttling.

- `max_tick_rate` (int32): [Read-Write] Values >= 1.
The maximum tick rate we allow. If this is set then we can potentially go over budget, but keep quality of individual meshes to a reasonable level.

- `max_ticked_offsreen_components` (int32): [Read-Write] Values >= 1
The maximum number of offscreen components we tick (most significant first)

- `min_quality` (float): [Read-Write] Values [0.0, 1.0].
The minimum quality metric allowed. Quality is determined simply by NumComponentsTickingThisFrame / NumComponentsThatWeNeedToTick.
If this is anything other than 0.0 then we can potentially go over our time budget.

- `reduced_work_throttle_max_in_frames` (int32): [Read-Write] Range [1, 255].
Prevents reduced work from changing too often due to system and load noise. Max value used when under budget pressure.

- `reduced_work_throttle_max_per_frame` (int32): [Read-Write] Range [1, 255].
Controls the max number of components that are switched to/from reduced work per tick.

- `reduced_work_throttle_min_in_frames` (int32): [Read-Write] Range [1, 255].
Prevents reduced work from changing too often due to system and load noise. Min value used when over budget pressure (i.e. aggressive reduction).

- `state_change_throttle_in_frames` (int32): [Read-Write] Range [1, 128]
Prevents throttle values from changing too often due to system and load noise.

- `work_unit_smoothing_speed` (float): [Read-Write] Values > 0.1.
The speed at which the average work unit converges on the measured amount.



---

_property_ `always_tick_falloff_aggression`: float

[Read-Write] Range [0.1, 0.9].
Controls the rate at which ‘always ticked’ components falloff under load.
Higher values mean that we reduce the number of always ticking components by a larger amount when the allocated time budget is exceeded.

**Type:**

( float)


---

_property_ `auto_calculated_significance_max_distance`: float

[Read-Write] Range > 1.0.
Controls the distance at which auto-calculated significance for budgeted components bottoms out. Components
within the distance 1 -> Max will have significance mapped 1 -> 0, outside of MaxDistance significance will be zero.

**Type:**

( float)


---

_property_ `budget_factor_before_aggressive_reduced_work`: float

[Read-Write] Range > 1.
Reduced work will be applied more rapidly when budget pressure goes over this amount.

**Type:**

( float)


---

_property_ `budget_factor_before_reduced_work`: float

[Read-Write] Range > 1
Reduced work will be delayed until budget pressure goes over this amount.

**Type:**

( float)


---

_property_ `budget_factor_before_reduced_work_epsilon`: float

[Read-Write] Range > 0.0.
Increased work will be delayed until budget pressure goes under BudgetFactorBeforeReducedWork minus this amount.

**Type:**

( float)


---

_property_ `budget_in_ms`: float

[Read-Write] Values > 0.1.
The time in milliseconds that we allocate for skeletal mesh work to be performed.
When overbudget various other parameters come into play, such as AlwaysTickFalloffAggression and InterpolationFalloffAggression.

**Type:**

( float)


---

_property_ `budget_pressure_before_emergency_reduced_work`: float

[Read-Write] Range > 0.0.
Controls the budget pressure where emergency reduced work (applied to all components except those that are bAlwaysTick).

**Type:**

( float)


---

_property_ `budget_pressure_smoothing_speed`: float

[Read-Write] Range > 0.0.
How much to smooth the budget pressure value used to throttle reduced work.

**Type:**

( float)


---

_property_ `initial_estimated_work_unit_time_ms`: float

[Read-Write] Values > 0.0.
Controls the time in milliseconds we expect, on average, for a skeletal mesh component to execute.
The value only applies for the first tick of a component, after which we use the real time the tick takes.

**Type:**

( float)


---

_property_ `interpolation_falloff_aggression`: float

[Read-Write] Range [0.1, 0.9].
Controls the rate at which interpolated components falloff under load.
Higher values mean that we reduce the number of interpolated components by a larger amount when the allocated time budget is exceeded.
Components are only interpolated when the time budget is exceeded.

**Type:**

( float)


---

_property_ `interpolation_max_rate`: int

[Read-Write] Values > 1.
Controls the rate at which ticks happen when interpolating.

**Type:**

(int32)


---

_property_ `interpolation_tick_multiplier`: float

[Read-Write] Range [0.1, 0.9].
Controls the expected value an amortized interpolated tick will take compared to a ‘normal’ tick.

**Type:**

( float)


---

_property_ `max_interpolated_components`: int

[Read-Write] Range >= 0.
Max number of components to interpolate before we start throttling.

**Type:**

(int32)


---

_property_ `max_tick_rate`: int

[Read-Write] Values >= 1.
The maximum tick rate we allow. If this is set then we can potentially go over budget, but keep quality of individual meshes to a reasonable level.

**Type:**

(int32)


---

_property_ `max_ticked_offsreen_components`: int

[Read-Write] Values >= 1
The maximum number of offscreen components we tick (most significant first)

**Type:**

(int32)


---

_property_ `min_quality`: float

[Read-Write] Values [0.0, 1.0].
The minimum quality metric allowed. Quality is determined simply by NumComponentsTickingThisFrame / NumComponentsThatWeNeedToTick.
If this is anything other than 0.0 then we can potentially go over our time budget.

**Type:**

( float)


---

_property_ `reduced_work_throttle_max_in_frames`: int

[Read-Write] Range [1, 255].
Prevents reduced work from changing too often due to system and load noise. Max value used when under budget pressure.

**Type:**

(int32)


---

_property_ `reduced_work_throttle_max_per_frame`: int

[Read-Write] Range [1, 255].
Controls the max number of components that are switched to/from reduced work per tick.

**Type:**

(int32)


---

_property_ `reduced_work_throttle_min_in_frames`: int

[Read-Write] Range [1, 255].
Prevents reduced work from changing too often due to system and load noise. Min value used when over budget pressure (i.e. aggressive reduction).

**Type:**

(int32)


---

_property_ `state_change_throttle_in_frames`: int

[Read-Write] Range [1, 128]
Prevents throttle values from changing too often due to system and load noise.

**Type:**

(int32)


---

_property_ `work_unit_smoothing_speed`: float

[Read-Write] Values > 0.1.
The speed at which the average work unit converges on the measured amount.

**Type:**

( float)

### Table of Contents

- `unreal.AnimationBudgetAllocatorParameters`
  - `AnimationBudgetAllocatorParameters`
    - `AnimationBudgetAllocatorParameters.always_tick_falloff_aggression`
    - `AnimationBudgetAllocatorParameters.auto_calculated_significance_max_distance`
    - `AnimationBudgetAllocatorParameters.budget_factor_before_aggressive_reduced_work`
    - `AnimationBudgetAllocatorParameters.budget_factor_before_reduced_work`
    - `AnimationBudgetAllocatorParameters.budget_factor_before_reduced_work_epsilon`
    - `AnimationBudgetAllocatorParameters.budget_in_ms`
    - `AnimationBudgetAllocatorParameters.budget_pressure_before_emergency_reduced_work`
    - `AnimationBudgetAllocatorParameters.budget_pressure_smoothing_speed`
    - `AnimationBudgetAllocatorParameters.initial_estimated_work_unit_time_ms`
    - `AnimationBudgetAllocatorParameters.interpolation_falloff_aggression`
    - `AnimationBudgetAllocatorParameters.interpolation_max_rate`
    - `AnimationBudgetAllocatorParameters.interpolation_tick_multiplier`
    - `AnimationBudgetAllocatorParameters.max_interpolated_components`
    - `AnimationBudgetAllocatorParameters.max_tick_rate`
    - `AnimationBudgetAllocatorParameters.max_ticked_offsreen_components`
    - `AnimationBudgetAllocatorParameters.min_quality`
    - `AnimationBudgetAllocatorParameters.reduced_work_throttle_max_in_frames`
    - `AnimationBudgetAllocatorParameters.reduced_work_throttle_max_per_frame`
    - `AnimationBudgetAllocatorParameters.reduced_work_throttle_min_in_frames`
    - `AnimationBudgetAllocatorParameters.state_change_throttle_in_frames`
    - `AnimationBudgetAllocatorParameters.work_unit_smoothing_speed`