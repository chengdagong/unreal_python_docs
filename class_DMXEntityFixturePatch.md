# unreal.DMXEntityFixturePatch

```python
class unreal.DMXEntityFixturePatch(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``DMXEntity``


A DMX fixture patch that can be patch to channels in a DMX Universe via the DMX Library Editor.

Use in DMXComponent or call SetReceiveDMXEnabled with ‘true’ to enable receiving DMX.

**C++ Source:**

- **Plugin**: DMXEngine

- **Module**: DMXRuntime

- **File**: DMXEntityFixturePatch.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `active_mode` (int32): [Read-Write] The Index of the Mode in the Fixture Type the Patch uses

- `auto_assign_address` (bool): [Read-Write] DEPRECATED 5.1
deprecated: bAutoAssignAddress and related members are deprecated. Auto assign is now only a method in FDMXEditorUtils and should be applied on demand.

- `auto_starting_address` (int32): [Read-Write] DEPRECATED 5.1
deprecated: bAutoAssignAddress and related members are deprecated. Auto assign is now only a method in FDMXEditorUtils and should be applied on demand.

- `custom_tags` (Array[Name]): [Read-Write] Custom tags for filtering patches

- `default_transform` (Transform): [Read-Write] The transform used when the DMX Library is spawned in a level.

When the DMX Library is exported as an MVR file, this transform is used unless the ‘Use Transforms from Level’ export option is checked.

- `editor_color` (LinearColor): [Read-Write] Color when displayed in the fixture patch editor

- `fixture_id` (int32): [Read-Only] The Fixture ID of this patch

- `manual_starting_address` (int32): [Read-Write] DEPRECATED 5.1
deprecated: bAutoAssignAddress and related members are deprecated. Auto assign is now only a method in FDMXEditorUtils and should be applied on demand.

- `mvr_fixture_uuid` (Guid): [Read-Only] The MVR Fixture UUID

- `name` (str): [Read-Write]

- `on_fixture_patch_received_dmx` (DMXOnFixturePatchReceivedDMXDelegate): [Read-Write] Returns a delegate broadcast when the fixture patch received DMX.
This event only fires when any attribute value changed.
Use GetAttributeValues or GetNormalizedAttributeValues to get unchanged values.

- `parent_fixture_type_template` (DMXEntityFixtureType): [Read-Only] The Fixture Type that defines the DMX channel layout of this Fixture Patch

- `receive_dmx_in_editor` (bool): [Read-Write] If true, the patch receives dmx and raises the OnFixturePatchReceivedDMX events in editor.
NOTE: If ‘All Fixture Patches receive DMX in editor’ is set to true in Project Settings -> Plugins -> DMX, this setting here is ignored.

- `starting_channel` (int32): [Read-Write] Starting Channel of the Patch

- `universe_id` (int32): [Read-Write] The local universe of the patch



---

_property_ `active_mode`: int

[Read-Only] The Index of the Mode in the Fixture Type the Patch uses

**Type:**

(int32)


---

_property_ `auto_assign_address`: bool

[Read-Write] DEPRECATED 5.1
deprecated: bAutoAssignAddress and related members are deprecated. Auto assign is now only a method in FDMXEditorUtils and should be applied on demand.

**Type:**

( bool)


---

_property_ `auto_starting_address`: int

[Read-Write] DEPRECATED 5.1
deprecated: bAutoAssignAddress and related members are deprecated. Auto assign is now only a method in FDMXEditorUtils and should be applied on demand.

**Type:**

(int32)


---

**contains_attribute**( _function_attribute_) → `bool`

Returns true if the Fixture Patch contains the specified attribute and can use it to send and receive DMX

Parameters:

**function\_attribute** ( _DMXAttributeName_)

Return type:

bool


---

**convert_attribute_map_to_raw_map**( _function_map_) → `Map[int32,uint8]`

Converts a map of Attribute Names with their DMX values to a map of DMX channels and with their DMX Values.

Parameters:

**function\_map** ( _Map_ _\_ [_DMXAttributeName_ _,_ _int32_ _]_)

Return type:

Map[int32, uint8]


---

**convert_raw_map_to_attribute_map**( _raw_map_) → `Map\ [DMXAttributeName,int32]`

Convert Raw Map to Attribute Map
deprecated: Deprecated 4.27. Please use DMXSubsystem’s Bytes to Int instead, then create a map from that with Attribute Names .

Parameters:

**raw\_map** ( _Map_ _[_ _int32_ _,_ _uint8_ _]_)

Return type:

Map\ [DMXAttributeName, int32]


---

**convert_to_valid_map**( _function_map_) → `Map\ [DMXAttributeName,int32]`

Removes any Attribute Name that can not be sent or received by a Fixture Patch from an Attribute Name to DMX Value Map

Parameters:

**function\_map** ( _Map_ _\_ [_DMXAttributeName_ _,_ _int32_ _]_)

Return type:

Map\ [DMXAttributeName, int32]


---

_classmethod_ create_fixture_patch_in_library( _construction_params_, _desired_name=''_, _mark_dmx_library_dirty=True_)→DMXEntityFixturePatch

Creates a new Fixture Patch in the DMX Library using the specified Fixture Type

Parameters:

- **construction\_params** ( _DMXEntityFixturePatchConstructionParams_)

- **desired\_name** ( _str_)

- **mark\_dmx\_library\_dirty** ( _bool_)


Return type:

DMXEntityFixturePatch


---

_property_ `custom_tags`: None

[Read-Only] Custom tags for filtering patches

**Type:**

( Array\ [Name])


---

_property_ `default_transform`: Transform

[Read-Write] The transform used when the DMX Library is spawned in a level.

When the DMX Library is exported as an MVR file, this transform is used unless the ‘Use Transforms from Level’ export option is checked.

**Type:**

( Transform)


---

_property_ `editor_color`: LinearColor

[Read-Only] Color when displayed in the fixture patch editor

**Type:**

( LinearColor)


---

_property_ `fixture_id`: int

[Read-Only] The Fixture ID of this patch

**Type:**

(int32)


---

**get_all_attributes_in_active_mode**() → `Array\ [DMXAttributeName]`

Returns an array of attributes for the currently active mode.
Attributes outside the Active Mode’s channel span range are ignored.

Return type:

Array\ [DMXAttributeName]


---

**get_all_matrix_cells**() → `Array[DMXCell]orNone`

Gets all matrix cells

Returns:

cells (Array[DMXCell]):

Return type:

Array\ [DMXCell] or None


---

**get_attribute_channel_assignments**() → `Map\ [DMXAttributeName,int32]`

Returns a map of Attributes and their assigned channels

Return type:

Map\ [DMXAttributeName, int32]


---

**get_attribute_default_map**() → `Map\ [DMXAttributeName,int32]`

Returns a map of function names and default values.
Functions outside the Active Mode’s channel span range are ignored.

Return type:

Map\ [DMXAttributeName, int32]


---

**get_attribute_functions_map**() → `Map\ [DMXAttributeName, DMXFixtureFunction]`

Returns a map of attributes and function names.
Attributes outside the Active Mode’s channel span range are ignored.

Return type:

Map\ [DMXAttributeName, DMXFixtureFunction]


---

**get_attribute_signal_formats**() → `Map\ [DMXAttributeName, DMXFixtureSignalFormat]`

Returns a map of function names and their Data Types.

Return type:

Map\ [DMXAttributeName, DMXFixtureSignalFormat]

get\_attribute\_value( _attribute)->(int32_, _success=bool_)

Retrieves the value of an Attribute. Will fail and return 0 if the Attribute doesn’t exist.

Parameters:

**attribute** ( _DMXAttributeName_) – The Attribute to try to get the value from.

Returns:

The value of the Function mapped to the selected Attribute, if found.

success (bool): Whether the Attribute was found in this Fixture Patch

Return type:

bool


---

**get_attribute_values**() → `Map\ [DMXAttributeName,int32]`

Returns the value of each attribute, or zero if no value was ever received.

Returns:

attribute\_values (Map[DMXAttributeName, int32]):

Return type:

Map\ [DMXAttributeName, int32]


---

**get_attributes_values**() → `None`

deprecated: ‘get\_attributes\_values’ was renamed to ‘get\_attribute\_values’.


---

**get_cell_attributes**() → `Array[DMXAttributeName]orNone`

Gets all attributes names of a cell

Returns:

cell\_attributes (Array[DMXAttributeName]):

Return type:

Array\ [DMXAttributeName] or None


---

**get_channel_span**() → `int32`

Returns the number of channels this Patch occupies with the Fixture functions from its Active Mode or 0 if the patch has no valid Active Mode

Return type:

int32


---

**get_ending_channel**() → `int32`

Returns the last channel of the patch

Return type:

int32


---

**get_matrix_cell**( _cell_coordinate_) → `DMXCellorNone`

Cell coordinate X/Y

Parameters:

**cell\_coordinate** ( _IntPoint_)

Returns:

cell (DMXCell):

Return type:

DMXCell or None


---

**get_matrix_cell_channels_absolute**( _cell_coordinate_) → `Map[DMXAttributeName,int32]orNone`

Cell coordinate X/Y

Parameters:

**cell\_coordinate** ( _IntPoint_)

Returns:

attribute\_channel\_map (Map[DMXAttributeName, int32]):

Return type:

Map\ [DMXAttributeName, int32] or None


---

**get_matrix_cell_channels_absolute_with_validation**( _cell_coordinate_) → `Map[DMXAttributeName,int32]orNone`

Cell coordinate X/Y

Parameters:

**cell\_coordinate** ( _IntPoint_)

Returns:

out\_attribute\_channel\_map (Map[DMXAttributeName, int32]):

Return type:

Map\ [DMXAttributeName, int32] or None


---

**get_matrix_cell_channels_relative**( _cell_coordinate_) → `Map[DMXAttributeName,int32]orNone`

Cell coordinate X/Y

Parameters:

**cell\_coordinate** ( _IntPoint_)

Returns:

attribute\_channel\_map (Map[DMXAttributeName, int32]):

Return type:

Map\ [DMXAttributeName, int32] or None


---

**get_matrix_cell_values**( _cell_coordinate_) → `Map[DMXAttributeName,int32]orNone`

Cell coordinate X/Y

Parameters:

**cell\_coordinate** ( _IntPoint_)

Returns:

value\_per\_attribute (Map[DMXAttributeName, int32]):

Return type:

Map\ [DMXAttributeName, int32] or None


---

**get_matrix_properties**() → `DMXFixtureMatrixorNone`

Gets the Matrix Fixture properties, returns false if the patch is not using a matrix fixture

Returns:

matrix\_properties (DMXFixtureMatrix):

Return type:

DMXFixtureMatrix or None

get\_normalized\_attribute\_value( _attribute)->(float_, _success=bool_)

Retrieves the normalized value of an Attribute. Will fail and return 0 if the Attribute doesn’t exist.
deprecated: Deprecated 4.26. Use GetNormalizedAttributeValue instead. Note, new method returns normalized values!

Parameters:

**attribute** ( _DMXAttributeName_) – The Attribute to try to get the value from.

Returns:

The value of the Function mapped to the selected Attribute, if found.

success (bool): Whether the Attribute was found in this Fixture Patch

Return type:

bool


---

**get_normalized_attribute_values**() → `DMXNormalizedAttributeValueMap`

Returns the normalized value of each attribute, or zero if no value was ever received.

Returns:

normalized\_attributes\_values (DMXNormalizedAttributeValueMap):

Return type:

DMXNormalizedAttributeValueMap


---

**get_normalized_attributes_values**() → `DMXNormalizedAttributeValueMap`

deprecated: ‘get\_normalized\_attributes\_values’ was renamed to ‘get\_normalized\_attribute\_values’.


---

**get_normalized_matrix_cell_values**( _cell_coordinate_) → `Map[DMXAttributeName,float]orNone`

Cell coordinate X/Y

Parameters:

**cell\_coordinate** ( _IntPoint_)

Returns:

normalized\_value\_per\_attribute (Map[DMXAttributeName, float]):

Return type:

Map\ [DMXAttributeName, float] or None


---

**get_relevant_controllers**() → `Array\ [DMXEntityController]`

Get Relevant Controllers
deprecated: Deprecated 4.27. Controllers are replaced with DMX Ports.

Return type:

Array\ [DMXEntityController]


---

**get_remote_universe**() → `int32`

Get Remote Universe
deprecated: Deprecated 4.27. No clear remote universe can be deduced from controllers (before 4.27) or ports (from 4.27 on).

Return type:

int32


---

**get_starting_channel**() → `int32`

Return the starting channel

Return type:

int32


---

**is_in_controller_range**( _controller_) → `bool`

Is in Controller Range
deprecated: Deprecated 4.27. Controllers are replaced with DMX Ports.

Parameters:

**controller** ( _DMXEntityController_)

Return type:

bool


---

**is_in_controllers_range**( _controllers_) → `bool`

Is in Controllers Range
deprecated: Deprecated 4.27. Controllers are replaced with DMX Ports.

Parameters:

**controllers** ( _Array_ _\_ [_DMXEntityController_ _]_)

Return type:

bool


---

**is_map_valid**( _function_map_) → `bool`

Returns true if the Fixture Patch contains all Attributes in an Attribute Name to DMX Value Map.

Parameters:

**function\_map** ( _Map_ _\_ [_DMXAttributeName_ _,_ _int32_ _]_)

Return type:

bool


---

_property_ `manual_starting_address`: int

[Read-Write] DEPRECATED 5.1
deprecated: bAutoAssignAddress and related members are deprecated. Auto assign is now only a method in FDMXEditorUtils and should be applied on demand.

**Type:**

(int32)


---

_property_ `mvr_fixture_uuid`: Guid

[Read-Only] The MVR Fixture UUID

**Type:**

( Guid)

_property_ on\_fixture\_patch\_received\_dmx _:DMXOnFixturePatchReceivedDMXDelegate_

[Read-Write] Returns a delegate broadcast when the fixture patch received DMX.
This event only fires when any attribute value changed.
Use GetAttributeValues or GetNormalizedAttributeValues to get unchanged values.

**Type:**

(DMXOnFixturePatchReceivedDMXDelegate)


---

_property_ `parent_fixture_type_template`: DMXEntityFixtureType

[Read-Only] The Fixture Type that defines the DMX channel layout of this Fixture Patch

**Type:**

( DMXEntityFixtureType)


---

_property_ `receive_dmx_in_editor`: bool

[Read-Only] If true, the patch receives dmx and raises the OnFixturePatchReceivedDMX events in editor.
NOTE: If ‘All Fixture Patches receive DMX in editor’ is set to true in Project Settings -> Plugins -> DMX, this setting here is ignored.

**Type:**

( bool)


---

_classmethod_ remove_fixture_patch_from_library( _fixture_patch_ref_)→None

Removes a fixture patch from the DMX Library

Parameters:

**fixture\_patch\_ref** ( _DMXEntityFixturePatchRef_)


---

**send_default_values**() → `None`

Sends the default value for all attributes, including matrix attributes.
Note, calls will not be considered by the DMX Conflict Monitor.


---

**send_dmx**( _attribute_map_) → `None`

Send DMX using attribute names and integer values.

Parameters:

**attribute\_map** ( _Map_ _\_ [_DMXAttributeName_ _,_ _int32_ _]_)


---

**send_matrix_cell_value**( _cell_coordinate_, _attribute_, _value_) → `bool`

Cell coordinate X/Y

Parameters:

- **cell\_coordinate** ( _IntPoint_)

- **attribute** ( _DMXAttributeName_)

- **value** ( _int32_)


Return type:

bool


---

**send_matrix_cell_value_with_attribute_map**( _cell_coordinate_, _attribute_, _value_, _attribute_name_channel_map_) → `bool`

Cell coordinate X/Y
deprecated: Deprecated due to ambigous arguments CellCoordinate and InAttributeNameChannelMap. Use SendMatrixCellValue or SendNormalizedMatrixCellValue instead.

Parameters:

- **cell\_coordinate** ( _IntPoint_)

- **attribute** ( _DMXAttributeName_)

- **value** ( _int32_)

- **attribute\_name\_channel\_map** ( _Map_ _\_ [_DMXAttributeName_ _,_ _int32_ _]_)


Return type:

bool


---

**send_normalized_matrix_cell_value**( _cell_coordinate_, _attribute_, _relative_value_) → `bool`

Cell coordinate X/Y

Parameters:

- **cell\_coordinate** ( _IntPoint_)

- **attribute** ( _DMXAttributeName_)

- **relative\_value** ( _float_)


Return type:

bool


---

**send_zero_values**() → `None`

Sends zeroes for all attributes, including matrix attributes.
Note, calls will not be considered by the DMX Conflict Monitor.


---

**set_fixture_type**( _new_fixture_type_) → `None`

Sets the fixture type this is using

Parameters:

**new\_fixture\_type** ( _DMXEntityFixtureType_)


---

**set_starting_channel**( _new_starting_channel_) → `None`

Sets the starting channel of the Fixture Patch.

Parameters:

**new\_starting\_channel** ( _int32_)


---

**set_universe_id**( _new_universe_id_) → `None`

Sets the Universe ID of the patch

Parameters:

**new\_universe\_id** ( _int32_)


---

_property_ `starting_channel`: int

[Read-Only] Starting Channel of the Patch

**Type:**

(int32)


---

_property_ `universe_id`: int

[Read-Only] The local universe of the patch

**Type:**

(int32)

### Table of Contents

- `unreal.DMXEntityFixturePatch`
  - `DMXEntityFixturePatch`
    - `DMXEntityFixturePatch.active_mode`
    - `DMXEntityFixturePatch.auto_assign_address`
    - `DMXEntityFixturePatch.auto_starting_address`
    - `DMXEntityFixturePatch.contains_attribute()`
    - `DMXEntityFixturePatch.convert_attribute_map_to_raw_map()`
    - `DMXEntityFixturePatch.convert_raw_map_to_attribute_map()`
    - `DMXEntityFixturePatch.convert_to_valid_map()`
    - `DMXEntityFixturePatch.create_fixture_patch_in_library()`
    - `DMXEntityFixturePatch.custom_tags`
    - `DMXEntityFixturePatch.default_transform`
    - `DMXEntityFixturePatch.editor_color`
    - `DMXEntityFixturePatch.fixture_id`
    - `DMXEntityFixturePatch.get_all_attributes_in_active_mode()`
    - `DMXEntityFixturePatch.get_all_matrix_cells()`
    - `DMXEntityFixturePatch.get_attribute_channel_assignments()`
    - `DMXEntityFixturePatch.get_attribute_default_map()`
    - `DMXEntityFixturePatch.get_attribute_functions_map()`
    - `DMXEntityFixturePatch.get_attribute_signal_formats()`
    - `DMXEntityFixturePatch.get_attribute_value()`
    - `DMXEntityFixturePatch.get_attribute_values()`
    - `DMXEntityFixturePatch.get_attributes_values()`
    - `DMXEntityFixturePatch.get_cell_attributes()`
    - `DMXEntityFixturePatch.get_channel_span()`
    - `DMXEntityFixturePatch.get_ending_channel()`
    - `DMXEntityFixturePatch.get_matrix_cell()`
    - `DMXEntityFixturePatch.get_matrix_cell_channels_absolute()`
    - `DMXEntityFixturePatch.get_matrix_cell_channels_absolute_with_validation()`
    - `DMXEntityFixturePatch.get_matrix_cell_channels_relative()`
    - `DMXEntityFixturePatch.get_matrix_cell_values()`
    - `DMXEntityFixturePatch.get_matrix_properties()`
    - `DMXEntityFixturePatch.get_normalized_attribute_value()`
    - `DMXEntityFixturePatch.get_normalized_attribute_values()`
    - `DMXEntityFixturePatch.get_normalized_attributes_values()`
    - `DMXEntityFixturePatch.get_normalized_matrix_cell_values()`
    - `DMXEntityFixturePatch.get_relevant_controllers()`
    - `DMXEntityFixturePatch.get_remote_universe()`
    - `DMXEntityFixturePatch.get_starting_channel()`
    - `DMXEntityFixturePatch.is_in_controller_range()`
    - `DMXEntityFixturePatch.is_in_controllers_range()`
    - `DMXEntityFixturePatch.is_map_valid()`
    - `DMXEntityFixturePatch.manual_starting_address`
    - `DMXEntityFixturePatch.mvr_fixture_uuid`
    - `DMXEntityFixturePatch.on_fixture_patch_received_dmx`
    - `DMXEntityFixturePatch.parent_fixture_type_template`
    - `DMXEntityFixturePatch.receive_dmx_in_editor`
    - `DMXEntityFixturePatch.remove_fixture_patch_from_library()`
    - `DMXEntityFixturePatch.send_default_values()`
    - `DMXEntityFixturePatch.send_dmx()`
    - `DMXEntityFixturePatch.send_matrix_cell_value()`
    - `DMXEntityFixturePatch.send_matrix_cell_value_with_attribute_map()`
    - `DMXEntityFixturePatch.send_normalized_matrix_cell_value()`
    - `DMXEntityFixturePatch.send_zero_values()`
    - `DMXEntityFixturePatch.set_fixture_type()`
    - `DMXEntityFixturePatch.set_starting_channel()`
    - `DMXEntityFixturePatch.set_universe_id()`
    - `DMXEntityFixturePatch.starting_channel`
    - `DMXEntityFixturePatch.universe_id`