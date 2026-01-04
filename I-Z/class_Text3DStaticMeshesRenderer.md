# unreal.Text3DStaticMeshesRenderer

```python
class unreal.Text3DStaticMeshesRenderer(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Text3DRendererBase``


Legacy/default renderer for Text3D
Each text character is rendered as a StaticMesh within its own StaticMeshComponent
Text3DComponent
\- Text3DRoot (Root)
— Text3DStaticMeshComponent (Character)

Eg: The text “Hello” will be rendered using 5 StaticMeshComponents

**C++ Source:**

- **Plugin**: Text3D

- **Module**: Text3D

- **File**: Text3DStaticMeshesRenderer.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `character_meshes` (Array[StaticMeshComponent]): [Read-Only] Each character mesh is held in these components

- `text_root` (SceneComponent): [Read-Only] Holds all character components



---

**get_glyph_count**() → `int32`

Gets the number of font glyphs that are currently used

Return type:

int32


---

**get_glyph_mesh_component**( _index_) → `StaticMeshComponent`

Gets the StaticMeshComponent of a glyph

Parameters:

**index** ( _int32_)

Return type:

StaticMeshComponent


---

**get_glyph_mesh_components**() → `Array\ [StaticMeshComponent]`

Gets all the glyph meshes

Return type:

Array\ [StaticMeshComponent]

### Table of Contents

- `unreal.Text3DStaticMeshesRenderer`
  - `Text3DStaticMeshesRenderer`
    - `Text3DStaticMeshesRenderer.get_glyph_count()`
    - `Text3DStaticMeshesRenderer.get_glyph_mesh_component()`
    - `Text3DStaticMeshesRenderer.get_glyph_mesh_components()`