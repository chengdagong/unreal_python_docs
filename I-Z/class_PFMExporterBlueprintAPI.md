# unreal.PFMExporterBlueprintAPI

```python
class unreal.PFMExporterBlueprintAPI(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Interface``


PFMExporter Blueprint API

**C++ Source:**

- **Plugin**: WarpUtils

- **Module**: PFMExporter

- **File**: IPFMExporterBlueprintAPI.h



---

**export_pfm**( _src_mesh_, _origin_, _width_, _height_, _file_name_) → `bool`

Generate PFM file from static mesh.
The UV channel must be defined, assigned range 0..1 used as screen surface.
Origin assigned by function arg, or by default used mesh parent.

Parameters:

- **src\_mesh** ( _StaticMeshComponent_) – Static mesh with assigned UV channel, used as export source of PFM file

- **origin** ( _SceneComponent_) – (Optional) Custom cave origin node, if not defined, used SrcMesh parent

- **width** ( _int32_) – Output PFM mesh texture width

- **height** ( _int32_) – Output PFM mesh texture height

- **file\_name** ( _str_) – Output PFM file name


Returns:

true, if success

Return type:

bool

### Table of Contents

- `unreal.PFMExporterBlueprintAPI`
  - `PFMExporterBlueprintAPI`
    - `PFMExporterBlueprintAPI.export_pfm()`