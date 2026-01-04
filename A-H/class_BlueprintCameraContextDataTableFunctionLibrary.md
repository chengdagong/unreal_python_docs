# unreal.BlueprintCameraContextDataTableFunctionLibrary

```python
class unreal.BlueprintCameraContextDataTableFunctionLibrary(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


Utility Blueprint functions for camera context data tables.

**C++ Source:**

- **Plugin**: GameplayCameras

- **Module**: GameplayCameras

- **File**: BlueprintCameraEvaluationDataRef.h


_classmethod_ get\_class\_data( _camera\_data_, _data\_id_)

Gets a value from the given camera context data table.

Parameters:

- **camera\_data** ( _BlueprintCameraEvaluationDataRef_)

- **data\_id** ( _CameraContextDataID_)


Return type:

type( Class)


---

_classmethod_ get_enum_data( _camera_data_, _data_id_, _enum_type_)→uint8

Gets a value from the given camera context data table.

Parameters:

- **camera\_data** ( _BlueprintCameraEvaluationDataRef_)

- **data\_id** ( _CameraContextDataID_)

- **enum\_type** ( _Enum_)


Return type:

uint8


---

_classmethod_ get_name_data( _camera_data_, _data_id_)→Name

Gets a value from the given camera context data table.

Parameters:

- **camera\_data** ( _BlueprintCameraEvaluationDataRef_)

- **data\_id** ( _CameraContextDataID_)


Return type:

Name


---

_classmethod_ get_object_data( _camera_data_, _data_id_)→Object

Gets a value from the given camera context data table.

Parameters:

- **camera\_data** ( _BlueprintCameraEvaluationDataRef_)

- **data\_id** ( _CameraContextDataID_)


Return type:

Object


---

_classmethod_ get_string_data( _camera_data_, _data_id_)→str

Gets a value from the given camera context data table.

Parameters:

- **camera\_data** ( _BlueprintCameraEvaluationDataRef_)

- **data\_id** ( _CameraContextDataID_)


Return type:

str


---

_classmethod_ get_struct_data( _camera_data_, _data_id_, _data_struct_type_)→InstancedStruct

Gets a value from the given camera context data table.

Parameters:

- **camera\_data** ( _BlueprintCameraEvaluationDataRef_)

- **data\_id** ( _CameraContextDataID_)

- **data\_struct\_type** ( _ScriptStruct_)


Return type:

InstancedStruct


---

_classmethod_ set_class_data( _camera_data_, _data_id_, _data_)→bool

Sets a value in the given camera context data table.

Parameters:

- **camera\_data** ( _BlueprintCameraEvaluationDataRef_)

- **data\_id** ( _CameraContextDataID_)

- **data** ( _type_ _(_ _Class_ _)_)


Return type:

bool


---

_classmethod_ set_enum_data( _camera_data_, _data_id_, _enum_type_, _data_)→bool

Sets a value in the given camera context data table.

Parameters:

- **camera\_data** ( _BlueprintCameraEvaluationDataRef_)

- **data\_id** ( _CameraContextDataID_)

- **enum\_type** ( _Enum_)

- **data** ( _uint8_)


Return type:

bool


---

_classmethod_ set_name_data( _camera_data_, _data_id_, _data_)→bool

Sets a value in the given camera context data table.

Parameters:

- **camera\_data** ( _BlueprintCameraEvaluationDataRef_)

- **data\_id** ( _CameraContextDataID_)

- **data** ( _Name_)


Return type:

bool


---

_classmethod_ set_object_data( _camera_data_, _data_id_, _data_)→bool

Sets a value in the given camera context data table.

Parameters:

- **camera\_data** ( _BlueprintCameraEvaluationDataRef_)

- **data\_id** ( _CameraContextDataID_)

- **data** ( _Object_)


Return type:

bool


---

_classmethod_ set_string_data( _camera_data_, _data_id_, _data_)→bool

Sets a value in the given camera context data table.

Parameters:

- **camera\_data** ( _BlueprintCameraEvaluationDataRef_)

- **data\_id** ( _CameraContextDataID_)

- **data** ( _str_)


Return type:

bool


---

_classmethod_ set_struct_data( _camera_data_, _data_id_, _data_)→bool

Sets a value in the given camera context data table.

Parameters:

- **camera\_data** ( _BlueprintCameraEvaluationDataRef_)

- **data\_id** ( _CameraContextDataID_)

- **data** ( _InstancedStruct_)


Return type:

bool

### Table of Contents

- `unreal.BlueprintCameraContextDataTableFunctionLibrary`
  - `BlueprintCameraContextDataTableFunctionLibrary`
    - `BlueprintCameraContextDataTableFunctionLibrary.get_class_data()`
    - `BlueprintCameraContextDataTableFunctionLibrary.get_enum_data()`
    - `BlueprintCameraContextDataTableFunctionLibrary.get_name_data()`
    - `BlueprintCameraContextDataTableFunctionLibrary.get_object_data()`
    - `BlueprintCameraContextDataTableFunctionLibrary.get_string_data()`
    - `BlueprintCameraContextDataTableFunctionLibrary.get_struct_data()`
    - `BlueprintCameraContextDataTableFunctionLibrary.set_class_data()`
    - `BlueprintCameraContextDataTableFunctionLibrary.set_enum_data()`
    - `BlueprintCameraContextDataTableFunctionLibrary.set_name_data()`
    - `BlueprintCameraContextDataTableFunctionLibrary.set_object_data()`
    - `BlueprintCameraContextDataTableFunctionLibrary.set_string_data()`
    - `BlueprintCameraContextDataTableFunctionLibrary.set_struct_data()`