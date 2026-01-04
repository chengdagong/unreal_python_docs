# unreal.MetaHumanGroomPipeline

```python
class unreal.MetaHumanGroomPipeline(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``MetaHumanItemPipeline``


MetaHuman Groom Pipeline

**C++ Source:**

- **Plugin**: MetaHumanCharacter

- **Module**: MetaHumanDefaultPipeline

- **File**: MetaHumanGroomPipeline.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `editor_pipeline` (MetaHumanItemEditorPipeline): [Read-Write]

- `override_materials` (Map[Name, MaterialInterface]): [Read-Write]

- `runtime_material_parameters` (Array[MetaHumanMaterialParameter]): [Read-Write]



---

_classmethod_ apply_groom_assembly_output_to_groom_component( _groom_assembly_output_, _groom_component_)→None

Apply Groom Assembly Output to Groom Component

Parameters:

- **groom\_assembly\_output** ( _MetaHumanGroomPipelineAssemblyOutput_)

- **groom\_component** ( _GroomComponent_)


### Table of Contents

- `unreal.MetaHumanGroomPipeline`
  - `MetaHumanGroomPipeline`
    - `MetaHumanGroomPipeline.apply_groom_assembly_output_to_groom_component()`