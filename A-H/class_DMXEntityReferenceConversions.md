# unreal.DMXEntityReferenceConversions

```python
class unreal.DMXEntityReferenceConversions(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


Extend type conversions to handle Entity Reference structs

**C++ Source:**

- **Plugin**: DMXEngine

- **Module**: DMXRuntime

- **File**: DMXEntityReference.h



---

_classmethod_ conv_controller_obj_to_ref( _controller_)→DMXEntityControllerRef

FDMXEntityControllerRef used as ret val is deprecated. Leave it to that to raise deprecated warnings in C++.
deprecated: Controllers are no longer used and deprecated in favor of the DMX Port System.

Parameters:

**controller** ( _DMXEntityController_)

Return type:

DMXEntityControllerRef


---

_classmethod_ conv_controller_ref_to_obj( _controller_ref_)→DMXEntityController

FDMXEntityControllerRef used in args is deprecated. Leave it to that to raise deprecated warnings in C++.
deprecated: Controllers are no longer used and deprecated in favor of the DMX Port System.

Parameters:

**controller\_ref** ( _DMXEntityControllerRef_)

Return type:

DMXEntityController


---

_classmethod_ conv_fixture_patch_obj_to_ref( _fixture_patch_)→DMXEntityFixturePatchRef

Conv Fixture Patch Obj to Ref

Parameters:

**fixture\_patch** ( _DMXEntityFixturePatch_)

Return type:

DMXEntityFixturePatchRef


---

_classmethod_ conv_fixture_patch_ref_to_obj( _fixture_patch_ref_)→DMXEntityFixturePatch

Conv Fixture Patch Ref to Obj

Parameters:

**fixture\_patch\_ref** ( _DMXEntityFixturePatchRef_)

Return type:

DMXEntityFixturePatch


---

_classmethod_ conv_fixture_type_obj_to_ref( _fixture_type_)→DMXEntityFixtureTypeRef

Conv Fixture Type Obj to Ref

Parameters:

**fixture\_type** ( _DMXEntityFixtureType_)

Return type:

DMXEntityFixtureTypeRef


---

_classmethod_ conv_fixture_type_ref_to_obj( _fixture_type_ref_)→DMXEntityFixtureType

Conv Fixture Type Ref to Obj

Parameters:

**fixture\_type\_ref** ( _DMXEntityFixtureTypeRef_)

Return type:

DMXEntityFixtureType

### Table of Contents

- `unreal.DMXEntityReferenceConversions`
  - `DMXEntityReferenceConversions`
    - `DMXEntityReferenceConversions.conv_controller_obj_to_ref()`
    - `DMXEntityReferenceConversions.conv_controller_ref_to_obj()`
    - `DMXEntityReferenceConversions.conv_fixture_patch_obj_to_ref()`
    - `DMXEntityReferenceConversions.conv_fixture_patch_ref_to_obj()`
    - `DMXEntityReferenceConversions.conv_fixture_type_obj_to_ref()`
    - `DMXEntityReferenceConversions.conv_fixture_type_ref_to_obj()`