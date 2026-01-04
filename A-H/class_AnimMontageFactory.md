# unreal.AnimMontageFactory

```python
class unreal.AnimMontageFactory(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Factory``


Anim Montage Factory

**C++ Source:**

- **Module**: UnrealEd

- **File**: AnimMontageFactory.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `asset_import_task` (AssetImportTask): [Read-Write] Task for importing file via script interfaces

- `automated_import_data` (AutomatedAssetImportData): [Read-Write] Data for how to import files via the automated command line importing interface

- `context_class` (type(Class)): [Read-Write] Class of the context object used to help create the object.

- `create_new` (bool): [Read-Write] The default value to return from CanCreateNew()

- `edit_after_new` (bool): [Read-Write] true if the associated editor should be opened after creating a new object.

- `editor_import` (bool): [Read-Write] true if the factory imports objects from files.

- `formats` (Array[str]): [Read-Write] List of formats supported by the factory. Each entry is of the form “ext;Description” where ext is the file extension.

- `source_animation` (AnimSequence): [Read-Write] Used when creating a montage from an AnimSequence, becomes the only AnimSequence contained

- `supported_class` (type(Class)): [Read-Write] The class manufactured by this factory.

- `supported_workflows` (uint8): [Read-Write] Which workflows are supported.

- `target_skeleton` (Skeleton): [Read-Write]

- `text` (bool): [Read-Write] true if the factory imports objects from text.



---

_property_ `source_animation`: AnimSequence

[Read-Write] Used when creating a montage from an AnimSequence, becomes the only AnimSequence contained

**Type:**

( AnimSequence)


---

_property_ `target_skeleton`: Skeleton

[Read-Write]

**Type:**

( Skeleton)

### Table of Contents

- `unreal.AnimMontageFactory`
  - `AnimMontageFactory`
    - `AnimMontageFactory.source_animation`
    - `AnimMontageFactory.target_skeleton`