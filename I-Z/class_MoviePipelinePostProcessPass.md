# unreal.MoviePipelinePostProcessPass

```python
class unreal.MoviePipelinePostProcessPass(enabled:bool=False, name:str='', material:MaterialInterface=Ellipsis, high_precision_output:bool=False, use_lossless_compression:bool=False)
```


**Bases:** ``StructBase``


Movie Pipeline Post Process Pass

**C++ Source:**

- **Plugin**: MovieRenderPipeline

- **Module**: MovieRenderPipelineRenderPasses

- **File**: MoviePipelineDeferredPasses.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `enabled` (bool): [Read-Write] Additional passes add a significant amount of render time. May produce multiple output files if using Screen Percentage.

- `high_precision_output` (bool): [Read-Write] Request output to be 32-bit, usually for data exports. Note that scene color precision is still defined by r.SceneColorFormat.

- `material` (MaterialInterface): [Read-Write] Material should be set to Post Process domain, and Blendable Location = After Tonemapping.
This will need bDisableMultisampleEffects enabled for pixels to line up(ie : no DoF, MotionBlur, TAA)

- `name` (str): [Read-Write] An optional name which which will identify this material in the file name. For MRQ, the material name will be included in the {render\_pass}
token. For Movie Render Graph, the material name will be used in {renderer\_sub\_name}. If a name is not specified here, the full name of the material
will be used in these tokens instead.

- `use_lossless_compression` (bool): [Read-Write] Whether this pass should use lossless compression in formats that support it. Should usually be turned on for passes that need a highly
accurate representation of the data (eg, depth).



---

_property_ `enabled`: bool

[Read-Write] Additional passes add a significant amount of render time. May produce multiple output files if using Screen Percentage.

**Type:**

( bool)


---

_property_ `high_precision_output`: bool

[Read-Write] Request output to be 32-bit, usually for data exports. Note that scene color precision is still defined by r.SceneColorFormat.

**Type:**

( bool)


---

_property_ `material`: MaterialInterface

[Read-Write] Material should be set to Post Process domain, and Blendable Location = After Tonemapping.
This will need bDisableMultisampleEffects enabled for pixels to line up(ie : no DoF, MotionBlur, TAA)

**Type:**

( MaterialInterface)


---

_property_ `name`: str

[Read-Write] An optional name which which will identify this material in the file name. For MRQ, the material name will be included in the {render\_pass}
token. For Movie Render Graph, the material name will be used in {renderer\_sub\_name}. If a name is not specified here, the full name of the material
will be used in these tokens instead.

**Type:**

( str)


---

_property_ `use_lossless_compression`: bool

[Read-Write] Whether this pass should use lossless compression in formats that support it. Should usually be turned on for passes that need a highly
accurate representation of the data (eg, depth).

**Type:**

( bool)

### Table of Contents

- `unreal.MoviePipelinePostProcessPass`
  - `MoviePipelinePostProcessPass`
    - `MoviePipelinePostProcessPass.enabled`
    - `MoviePipelinePostProcessPass.high_precision_output`
    - `MoviePipelinePostProcessPass.material`
    - `MoviePipelinePostProcessPass.name`
    - `MoviePipelinePostProcessPass.use_lossless_compression`