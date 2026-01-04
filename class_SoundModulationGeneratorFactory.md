# unreal.SoundModulationGeneratorFactory

```python
class unreal.SoundModulationGeneratorFactory(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Factory``


Sound Modulation Generator Factory

**C++ Source:**

- **Plugin**: AudioModulation

- **Module**: AudioModulationEditor

- **File**: SoundModulationGeneratorFactory.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `asset_import_task` (AssetImportTask): [Read-Write] Task for importing file via script interfaces

- `automated_import_data` (AutomatedAssetImportData): [Read-Write] Data for how to import files via the automated command line importing interface

- `context_class` (type(Class)): [Read-Write] Class of the context object used to help create the object.

- `create_new` (bool): [Read-Write] The default value to return from CanCreateNew()

- `edit_after_new` (bool): [Read-Write] true if the associated editor should be opened after creating a new object.

- `editor_import` (bool): [Read-Write] true if the factory imports objects from files.

- `formats` (Array[str]): [Read-Write] List of formats supported by the factory. Each entry is of the form “ext;Description” where ext is the file extension.

- `supported_class` (type(Class)): [Read-Write] The class manufactured by this factory.

- `supported_workflows` (uint8): [Read-Write] Which workflows are supported.

- `text` (bool): [Read-Write] true if the factory imports objects from text.


### Table of Contents

- `unreal.SoundModulationGeneratorFactory`
  - `SoundModulationGeneratorFactory`