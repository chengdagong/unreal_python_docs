# unreal.MovieSceneComposureExportPass

```python
class unreal.MovieSceneComposureExportPass
```


**Bases:** ``StructBase``


Export configuration options for a single internal pass on an ACompositingElement, or its output pass (where TransformPassName is None)

**C++ Source:**

- **Plugin**: Composure

- **Module**: Composure

- **File**: MovieSceneComposureExportTrack.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `exported_as` (Name): [Read-Write] The name to use for this pass when rendering out

- `rename_pass` (bool): [Read-Write] Whether to rename this pass when rendering out

- `transform_pass_name` (Name): [Read-Write] The name of the transform pass in the comp to export. None signifies the element’s output.


### Table of Contents

- `unreal.MovieSceneComposureExportPass`
  - `MovieSceneComposureExportPass`