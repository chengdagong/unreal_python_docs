# unreal.NiagaraDataInterfaceVectorCurve

```python
class unreal.NiagaraDataInterfaceVectorCurve(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``NiagaraDataInterfaceCurveBase``


Data Interface allowing sampling of vector curves.

**C++ Source:**

- **Plugin**: Niagara

- **Module**: Niagara

- **File**: NiagaraDataInterfaceVectorCurve.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `curve_asset` (CurveBase): [Read-Write]

- `expose_curve` (bool): [Read-Write] Generates a texture for the curve which can be exposed to material bindings.

- `exposed_name` (Name): [Read-Write] Sets a custom name for the binding to make it easier to identify.

- `optimize_lut` (bool): [Read-Write] Do we optimize the LUT, this saves memory but may introduce errors. Errors can be reduced modifying the threshold.

- `optimize_threshold` (float): [Read-Write] Threshold used to optimize the LUT.

- `override_optimize_threshold` (bool): [Read-Write]

- `use_lut` (bool): [Read-Write]

- `x_curve` (RichCurve): [Read-Write]

- `y_curve` (RichCurve): [Read-Write]

- `z_curve` (RichCurve): [Read-Write]


### Table of Contents

- `unreal.NiagaraDataInterfaceVectorCurve`
  - `NiagaraDataInterfaceVectorCurve`