# unreal.EditorValidatorSubsystem

```python
class unreal.EditorValidatorSubsystem(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``EditorSubsystem``


UEditorValidatorSubsystem manages all the asset validation in the engine.

The first validation handled is UObject::IsDataValid and its overridden functions.
Those validations require custom classes and are most suited to project-specific
classes.

The next validation set is of all registered UEditorValidationBases. These validators
have a function to determine if they can validate a given asset, and if they are
currently enabled. They are good candidates for validating engine classes or
very specific project logic.

Finally, this subsystem may be subclassed to change the overally behavior of
validation in your project. If a subclass exist in your project module, it will
supercede the engine validation subsystem.

**C++ Source:**

- **Plugin**: DataValidation

- **Module**: DataValidation

- **File**: EditorValidatorSubsystem.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `validate_on_save` (bool): [Read-Write] Whether it should validate assets on save inside the editor
deprecated: Use bValidateOnSave on UDataValidationSettings instead.



---

**add_validator**( _validator_) → `None`

- Adds a validator to the list, making sure it is a unique instance


Parameters:

**validator** ( _EditorValidatorBase_)

is\_asset\_valid( _asset\_data,validation\_usecase)->(DataValidationResult,validation\_errors=Array[Text],validation\_warnings=Array[Text]_)

Loads the object referred to by the provided AssetData and runs registered validators on it.
Does not add anything to any FMessageLog tabs.

Parameters:

- **asset\_data** ( _AssetData_)

- **validation\_usecase** ( _DataValidationUsecase_)


Returns:

Returns Valid if the object pointed to by AssetData contains valid data; returns Invalid if the object contains invalid data or does not exist; returns NotValidated if no validations was performed on the object

validation\_errors (Array[Text]):

validation\_warnings (Array[Text]):

Return type:

tuple

is\_object\_valid( _object,validation\_usecase)->(DataValidationResult,validation\_errors=Array[Text],validation\_warnings=Array[Text]_)

Runs registered validators on the provided object.
Does not add anything to any FMessageLog tabs.

Parameters:

- **object** ( _Object_)

- **validation\_usecase** ( _DataValidationUsecase_)


Returns:

Returns Valid if the object contains valid data; returns Invalid if the object contains invalid data; returns NotValidated if no validations was performed on the object

validation\_errors (Array[Text]):

validation\_warnings (Array[Text]):

Return type:

tuple


---

**remove_validator**( _validator_) → `None`

- Removes a validator

- Should be called during module shutdown if a validator was added.


Parameters:

**validator** ( _EditorValidatorBase_)

validate\_assets\_with\_settings( _asset\_data\_list_, _settings)->(int32_, _out\_results=ValidateAssetsResults_)

Called to validate assets from either the UI or a commandlet.
Loads the specified assets and runs all registered validators on them.
Populates the message log with errors and warnings with clickable links.

Parameters:

- **asset\_data\_list** ( _Array_ _\_ [_AssetData_ _]_)

- **settings** ( _ValidateAssetsSettings_) – Structure passing context and settings for ValidateAssetsWithSettings


Returns:

Number of assets with validation failures or warnings

out\_results (ValidateAssetsResults): More detailed information about the results of the validate assets command

Return type:

ValidateAssetsResults

validate\_changelist( _changelist_, _settings)->(DataValidationResult_, _out\_results=ValidateAssetsResults_)

Called to validate assets from either the UI or a commandlet.
Loads the specified assets and runs all registered validators on them.
Populates the message log with errors and warnings with clickable links.

Parameters:

- **changelist** ( _DataValidationChangelist_)

- **settings** ( _ValidateAssetsSettings_) – Structure passing context and settings for ValidateAssetsWithSettings


Returns:

Validation results for the changelist object itself

out\_results (ValidateAssetsResults): More detailed information about the results of the validate assets command

Return type:

ValidateAssetsResults

validate\_changelists( _changelists_, _settings)->(DataValidationResult_, _out\_results=ValidateAssetsResults_)

Validate Changelists

Parameters:

- **changelists** ( _Array_ _\_ [_DataValidationChangelist_ _]_)

- **settings** ( _ValidateAssetsSettings_)


Returns:

out\_results (ValidateAssetsResults):

Return type:

ValidateAssetsResults


---

_property_ `validate_on_save`: bool

[Read-Write] Whether it should validate assets on save inside the editor
deprecated: Use bValidateOnSave on UDataValidationSettings instead.

**Type:**

( bool)

### Table of Contents

- `unreal.EditorValidatorSubsystem`
  - `EditorValidatorSubsystem`
    - `EditorValidatorSubsystem.add_validator()`
    - `EditorValidatorSubsystem.is_asset_valid()`
    - `EditorValidatorSubsystem.is_object_valid()`
    - `EditorValidatorSubsystem.remove_validator()`
    - `EditorValidatorSubsystem.validate_assets_with_settings()`
    - `EditorValidatorSubsystem.validate_changelist()`
    - `EditorValidatorSubsystem.validate_changelists()`
    - `EditorValidatorSubsystem.validate_on_save`