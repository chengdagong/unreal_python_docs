# unreal.DMXEntityFixtureType

```python
class unreal.DMXEntityFixtureType(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``DMXEntity``


Class to describe a type of Fixture. Fixture Patches can be created from Fixture Types (see UDMXEntityFixturePatch::ParentFixtureTypeTemplate).

**C++ Source:**

- **Plugin**: DMXEngine

- **Module**: DMXRuntime

- **File**: DMXEntityFixtureType.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `actor_class_to_spawn` (Class): [Read-Write] The Actor Class that is spawned when the DMX Library dropped onto a Level.
Only Actors that implement the MVR Fixture Actor Interface can be used.

Can be left blank. If so, any Actor Class with the most matching Attributes will be spawned.

- `dmx_category` (DMXFixtureCategory): [Read-Write] The Category of the Fixture, useful for Filtering

- `dmx_import` (DMXImport): [Read-Write]
deprecated: Changed to a soft object pointer to reduce the memory footprint of Fixture Types. Please use GDTF Source instead.

- `export_generated_gdtf` (bool): [Read-Write] If checked, generates a new GDTF instead of exporting the imported GDTF. This adopts changes in editor but in most cases will result in data loss and is not recommended.

- `fixture_matrix_enabled` (bool): [Read-Write]
deprecated: FixtureMatrixEnabled is deprecated. Instead now each Mode has a FixtureMatrixEnabled property.

- `gdtf_source` (DMXImportGDTF): [Read-Write] The GDTF that initializes this Fixture Type. When changed, reinitializes with data from the GDTF.

- `input_modulators` (Array[DMXModulator]): [Read-Write] Modulators applied right before a patch of this type is received.
NOTE: Modulators only affect the patch’s normalized values! Untouched values are still available when accesing raw values.

- `modes` (Array[DMXFixtureMode]): [Read-Write]

- `name` (str): [Read-Write]



---

_classmethod_ create_fixture_type_in_library( _construction_params_, _desired_name=''_, _mark_dmx_library_dirty=True_)→DMXEntityFixtureType

Creates a new Fixture Type in the DMX Library

Parameters:

- **construction\_params** ( _DMXEntityFixtureTypeConstructionParams_)

- **desired\_name** ( _str_)

- **mark\_dmx\_library\_dirty** ( _bool_)


Return type:

DMXEntityFixtureType


---

_property_ `dmx_category`: DMXFixtureCategory

[Read-Only] The Category of the Fixture, useful for Filtering

**Type:**

( DMXFixtureCategory)


---

_property_ `dmx_import`: DMXImport

[Read-Only]
deprecated: Changed to a soft object pointer to reduce the memory footprint of Fixture Types. Please use GDTF Source instead.

**Type:**

( DMXImport)


---

_property_ `fixture_matrix_enabled`: bool

[Read-Write]
deprecated: FixtureMatrixEnabled is deprecated. Instead now each Mode has a FixtureMatrixEnabled property.

**Type:**

( bool)


---

_property_ `gdtf_source`: DMXImportGDTF

[Read-Only] The GDTF that initializes this Fixture Type. When changed, reinitializes with data from the GDTF.

**Type:**

( DMXImportGDTF)


---

_property_ `modes`: None

[Read-Only]

**Type:**

( Array\ [DMXFixtureMode])


---

_classmethod_ remove_fixture_type_from_library( _fixture_type_ref_)→None

Removes a Fixture Type from a DMX Library

Parameters:

**fixture\_type\_ref** ( _DMXEntityFixtureTypeRef_)


---

**set_modes_from_dmx_import**( _dmx_import_asset_) → `None`

Set Modes from DMXImport
deprecated: Setting GDTFs from blueprints was never fully supported and now deprecated. Instead please refer to the Create Fixture Type In DMX Library function.

Parameters:

**dmx\_import\_asset** ( _DMXImport_)

### Table of Contents

- `unreal.DMXEntityFixtureType`
  - `DMXEntityFixtureType`
    - `DMXEntityFixtureType.create_fixture_type_in_library()`
    - `DMXEntityFixtureType.dmx_category`
    - `DMXEntityFixtureType.dmx_import`
    - `DMXEntityFixtureType.fixture_matrix_enabled`
    - `DMXEntityFixtureType.gdtf_source`
    - `DMXEntityFixtureType.modes`
    - `DMXEntityFixtureType.remove_fixture_type_from_library()`
    - `DMXEntityFixtureType.set_modes_from_dmx_import()`