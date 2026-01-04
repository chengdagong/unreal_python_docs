# unreal.TextLibrary

```python
class unreal.TextLibrary(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


Kismet Text Library

**C++ Source:**

- **Module**: Engine

- **File**: KismetTextLibrary.h



---

_classmethod_ as_currency_base( _base_value_, _currency_code_)→Text

Generate an FText that represents the passed number as currency in the current culture.
BaseVal is specified in the smallest fractional value of the currency and will be converted for formatting according to the selected culture.
Keep in mind the CurrencyCode is completely independent of the culture it’s displayed in (and they do not imply one another).
For example: FText::AsCurrencyBase(650, TEXT(“EUR”)); would return an FText of “<EUR>6.50” in most English cultures (en\_US/en\_UK) and “6,50<EUR>” in Spanish (es\_ES) (where <EUR> is U+20AC)

Parameters:

- **base\_value** ( _int32_)

- **currency\_code** ( _str_)


Return type:

Text


---

_classmethod_ as_currency_float( _value_, _rounding_mode_, _always_sign=False_, _use_grouping=True_, _minimum_integral_digits=1_, _maximum_integral_digits=324_, _minimum_fractional_digits=0_, _maximum_fractional_digits=3_, _currency_code=''_)→Text

Converts a passed in float to a text formatted as a currency

Parameters:

- **value** ( _float_)

- **rounding\_mode** ( _RoundingMode_)

- **always\_sign** ( _bool_)

- **use\_grouping** ( _bool_)

- **minimum\_integral\_digits** ( _int32_)

- **maximum\_integral\_digits** ( _int32_)

- **minimum\_fractional\_digits** ( _int32_)

- **maximum\_fractional\_digits** ( _int32_)

- **currency\_code** ( _str_)


Return type:

Text


---

_classmethod_ as_currency_integer( _value_, _rounding_mode_, _always_sign=False_, _use_grouping=True_, _minimum_integral_digits=1_, _maximum_integral_digits=324_, _minimum_fractional_digits=0_, _maximum_fractional_digits=3_, _currency_code=''_)→Text

Converts a passed in integer to a text formatted as a currency

Parameters:

- **value** ( _int32_)

- **rounding\_mode** ( _RoundingMode_)

- **always\_sign** ( _bool_)

- **use\_grouping** ( _bool_)

- **minimum\_integral\_digits** ( _int32_)

- **maximum\_integral\_digits** ( _int32_)

- **minimum\_fractional\_digits** ( _int32_)

- **maximum\_fractional\_digits** ( _int32_)

- **currency\_code** ( _str_)


Return type:

Text


---

_classmethod_ as_date_date_time( _date_time_, _date_style=DateTimeStyle.DEFAULT_)→Text

Converts a passed in date & time to a text, formatted as a date using an invariant timezone. This will use the given date & time as-is, so it’s assumed to already be in the correct timezone.

Parameters:

- **date\_time** ( _DateTime_)

- **date\_style** ( _DateTimeStyle_)


Return type:

Text


---

_classmethod_ as_date_time_date_time( _in__, _date_style=DateTimeStyle.DEFAULT_, _time_style=DateTimeStyle.DEFAULT_)→Text

Converts a passed in date & time to a text, formatted as a date & time using an invariant timezone. This will use the given date & time as-is, so it’s assumed to already be in the correct timezone.

Parameters:

- **in** ( _DateTime_)

- **date\_style** ( _DateTimeStyle_)

- **time\_style** ( _DateTimeStyle_)


Return type:

Text


---

_classmethod_ as_memory( _num_bytes_, _unit_standard=MemoryUnitStandard.IEC_, _use_grouping=True_, _minimum_integral_digits=1_, _maximum_integral_digits=324_, _minimum_fractional_digits=0_, _maximum_fractional_digits=3_)→Text

Generate an FText that represents the passed number as a memory size in the current culture

Parameters:

- **num\_bytes** ( _int64_)

- **unit\_standard** ( _MemoryUnitStandard_)

- **use\_grouping** ( _bool_)

- **minimum\_integral\_digits** ( _int32_)

- **maximum\_integral\_digits** ( _int32_)

- **minimum\_fractional\_digits** ( _int32_)

- **maximum\_fractional\_digits** ( _int32_)


Return type:

Text


---

_classmethod_ as_percent_float( _value_, _rounding_mode_, _always_sign=False_, _use_grouping=True_, _minimum_integral_digits=1_, _maximum_integral_digits=324_, _minimum_fractional_digits=0_, _maximum_fractional_digits=3_)→Text

Converts a passed in float to a text, formatted as a percent

Parameters:

- **value** ( _float_)

- **rounding\_mode** ( _RoundingMode_)

- **always\_sign** ( _bool_)

- **use\_grouping** ( _bool_)

- **minimum\_integral\_digits** ( _int32_)

- **maximum\_integral\_digits** ( _int32_)

- **minimum\_fractional\_digits** ( _int32_)

- **maximum\_fractional\_digits** ( _int32_)


Return type:

Text


---

_classmethod_ as_time_date_time( _in__, _time_style=DateTimeStyle.DEFAULT_)→Text

Converts a passed in date & time to a text, formatted as a time using an invariant timezone. This will use the given date & time as-is, so it’s assumed to already be in the correct timezone.

Parameters:

- **in** ( _DateTime_)

- **time\_style** ( _DateTimeStyle_)


Return type:

Text


---

_classmethod_ as_time_zone_date_date_time( _date_time_, _time_zone=''_, _date_style=DateTimeStyle.DEFAULT_)→Text

Converts a passed in date & time to a text, formatted as a date using the given timezone (default is the local timezone). This will convert the given date & time from UTC to the given timezone (taking into account DST).

Parameters:

- **date\_time** ( _DateTime_)

- **time\_zone** ( _str_)

- **date\_style** ( _DateTimeStyle_)


Return type:

Text


---

_classmethod_ as_time_zone_date_time_date_time( _date_time_, _time_zone=''_, _date_style=DateTimeStyle.DEFAULT_, _time_style=DateTimeStyle.DEFAULT_)→Text

Converts a passed in date & time to a text, formatted as a date & time using the given timezone (default is the local timezone). This will convert the given date & time from UTC to the given timezone (taking into account DST).

Parameters:

- **date\_time** ( _DateTime_)

- **time\_zone** ( _str_)

- **date\_style** ( _DateTimeStyle_)

- **time\_style** ( _DateTimeStyle_)


Return type:

Text


---

_classmethod_ as_time_zone_time_date_time( _date_time_, _time_zone=''_, _time_style=DateTimeStyle.DEFAULT_)→Text

Converts a passed in date & time to a text, formatted as a time using the given timezone (default is the local timezone). This will convert the given date & time from UTC to the given timezone (taking into account DST).

Parameters:

- **date\_time** ( _DateTime_)

- **time\_zone** ( _str_)

- **time\_style** ( _DateTimeStyle_)


Return type:

Text


---

_classmethod_ as_timespan_timespan( _timespan_)→Text

Converts a passed in time span to a text, formatted as a time span

Parameters:

**timespan** ( _Timespan_)

Return type:

Text


---

_classmethod_ conv_bool_to_text( _bool_)→Text

Converts a boolean value to formatted text, either ‘true’ or ‘false’

Parameters:

**bool** ( _bool_)

Return type:

Text


---

_classmethod_ conv_byte_to_text( _value_)→Text

Converts a byte value to formatted text

Parameters:

**value** ( _uint8_)

Return type:

Text


---

_classmethod_ conv_color_to_text( _color_)→Text

Converts a linear color value to localized formatted text, in the form ‘(R=,G=,B=,A=)’

Parameters:

**color** ( _LinearColor_)

Return type:

Text


---

_classmethod_ conv_double_to_text( _value_, _rounding_mode_, _always_sign=False_, _use_grouping=True_, _minimum_integral_digits=1_, _maximum_integral_digits=324_, _minimum_fractional_digits=0_, _maximum_fractional_digits=3_)→Text

Converts a passed in double to text based on formatting options

Parameters:

- **value** ( _double_)

- **rounding\_mode** ( _RoundingMode_)

- **always\_sign** ( _bool_)

- **use\_grouping** ( _bool_)

- **minimum\_integral\_digits** ( _int32_)

- **maximum\_integral\_digits** ( _int32_)

- **minimum\_fractional\_digits** ( _int32_)

- **maximum\_fractional\_digits** ( _int32_)


Return type:

Text


---

_classmethod_ conv_float_to_text( _value:float_, _rounding_mode:RoundingMode_, _always_sign:bool=False_, _use_grouping:bool=True_, _minimum_integral_digits:int=1_, _maximum_integral_digits:int=324_, _minimum_fractional_digits:int=0_, _maximum_fractional_digits:int=3_)→Text

deprecated: ‘conv\_float\_to\_text’ was renamed to ‘conv\_double\_to\_text’.


---

_classmethod_ conv_int64_to_text( _value_, _always_sign=False_, _use_grouping=True_, _minimum_integral_digits=1_, _maximum_integral_digits=324_)→Text

Converts a passed in integer to text based on formatting options

Parameters:

- **value** ( _int64_)

- **always\_sign** ( _bool_)

- **use\_grouping** ( _bool_)

- **minimum\_integral\_digits** ( _int32_)

- **maximum\_integral\_digits** ( _int32_)


Return type:

Text


---

_classmethod_ conv_int_to_text( _value_, _always_sign=False_, _use_grouping=True_, _minimum_integral_digits=1_, _maximum_integral_digits=324_)→Text

Converts a passed in integer to text based on formatting options

Parameters:

- **value** ( _int32_)

- **always\_sign** ( _bool_)

- **use\_grouping** ( _bool_)

- **minimum\_integral\_digits** ( _int32_)

- **maximum\_integral\_digits** ( _int32_)


Return type:

Text


---

_classmethod_ conv_name_to_text( _name_)→Text

Converts Name to culture invariant text

Parameters:

**name** ( _Name_)

Return type:

Text


---

_classmethod_ conv_object_to_text( _obj_)→Text

Converts a UObject value to culture invariant text by calling the object’s GetName method

Parameters:

**obj** ( _Object_)

Return type:

Text


---

_classmethod_ conv_rotator_to_text( _rot_)→Text

Converts a rotator value to localized formatted text, in the form ‘P= Y= R=’

Parameters:

**rot** ( _Rotator_)

Return type:

Text


---

_classmethod_ conv_string_to_text( _string_)→Text

Converts string to culture invariant text. Use ‘Make Literal Text’ to create localizable text, or ‘Format’ if concatenating localized text

Parameters:

**string** ( _str_)

Return type:

Text


---

_classmethod_ conv_text_to_string( _text_)→str

Converts localizable text to the string

Parameters:

**text** ( _Text_)

Return type:

str


---

_classmethod_ conv_transform_to_text( _trans_)→Text

Converts a transform value to localized formatted text, in the form ‘Translation: X= Y= Z= Rotation: P= Y= R= Scale: X= Y= Z=’

Parameters:

**trans** ( _Transform_)

Return type:

Text


---

_classmethod_ conv_vector2d_to_text( _vec_)→Text

Converts a vector2d value to localized formatted text, in the form ‘X= Y=’

Parameters:

**vec** ( _Vector2D_)

Return type:

Text


---

_classmethod_ conv_vector_to_text( _vec_)→Text

Converts a vector value to localized formatted text, in the form ‘X= Y= Z=’

Parameters:

**vec** ( _Vector_)

Return type:

Text


---

_classmethod_ edit_text_property_source_string( _text_owner_, _property_name_, _source_string_, _emit_change_notify=True_)→bool

Edit the source string of the given text property, akin to what happens when editing a text property in a details panel.
This will attempt to preserve the existing ID of the text property being edited, or failing that will attempt to build a deterministic ID based on the object and property info.
note: This is an ADVANCED function that is ONLY safe to be used in environments where the modified text property will be gathered for localization (eg, in the editor, or a game mode that collects text properties to be localized).

Parameters:

- **text\_owner** ( _Object_) – The object that owns the given Text to be edited.

- **property\_name** ( _Name_) – The name of the text property to edit. This must be a property that exists on TextOwner.

- **source\_string** ( _str_) – The source string that the edited text property should use.

- **emit\_change\_notify** ( _bool_) – True to emit a pre/post edit change notify (in the editor). You should set this to false if editing text within a construction script.


Returns:

True if edit was possible, or false if not.

Return type:

bool


---

_classmethod_ equal_equal_ignore_case_text_text( _a_, _b_)→bool

Returns true if A and B are linguistically equal (A == B), ignoring case.

Parameters:

- **a** ( _Text_)

- **b** ( _Text_)


Return type:

bool


---

_classmethod_ equal_equal_text_text( _a_, _b_)→bool

Returns true if A and B are linguistically equal (A == B).

Parameters:

- **a** ( _Text_)

- **b** ( _Text_)


Return type:

bool


---

_classmethod_ find_text_in_live_table_advanced( _namespace_, _key_, _source_string=''_)→TextorNone

=== !! This is an ADVANCED function. USE WITH CAUTION !! ===

Attempt to dynamically reference an EXISTING Text via its active display string in the live table.
Note: This can ONLY find text that is currently localized (gathered, translated, and has an active display string in TextLocalizationManager). If you need to find a localizable but untranslated text, see ‘Make Literal Text’.
Note: Direct dynamic references to Text are EXTREMELY FRAGILE, and you may want to use a string table instead!

Parameters:

- **namespace** ( _str_) – The namespace of the text to find (if any).

- **key** ( _str_) – The key of the text to find.

- **source\_string** ( _str_) – If set (not empty) then the found text must also have been created from this source string.


Returns:

out\_text (Text):

Return type:

Text or None


---

_classmethod_ find_text_in_localization_table( _namespace:str_, _key:str_, _source_string:str=''_)→Text | None

deprecated: ‘find\_text\_in\_localization\_table’ was renamed to ‘find\_text\_in\_live\_table\_advanced’.


---

_classmethod_ get_empty_text()→Text

Returns an empty piece of text.

Return type:

Text


---

_classmethod_ get_text_id( _text_)→(out_namespace=str,out_key=str)orNone

Attempts to get the ID (namespace and key) used by the given text.

Parameters:

**text** ( _Text_)

Returns:

True if the namespace (which may be empty) and key were found, false otherwise.

out\_namespace (str):

out\_key (str):

Return type:

tuple or None


---

_classmethod_ get_text_source_string( _text_)→str

Get the (non-localized) source string of the given text.
note: For a generated text (eg, the result of a Format), this will deep build the source string as if the generation had run for the native language.

Parameters:

**text** ( _Text_)

Return type:

str

_classmethod_ is\_polyglot\_data\_valid( _polyglot\_data)->(is\_valid=bool_, _error\_message=Text_)

Check whether the given polyglot data is valid.

Parameters:

**polyglot\_data** ( _PolyglotTextData_)

Returns:

is\_valid (bool):

error\_message (Text):

Return type:

tuple


---

_classmethod_ make_invariant_text( _string_)→Text

Converts string to culture invariant text. Use ‘Make Literal Text’ to create localizable text, or ‘Format’ if concatenating localized text

Parameters:

**string** ( _str_)

Return type:

Text


---

_classmethod_ not_equal_ignore_case_text_text( _a_, _b_)→bool

Returns true if A and B are linguistically not equal (A != B), ignoring case.

Parameters:

- **a** ( _Text_)

- **b** ( _Text_)


Return type:

bool


---

_classmethod_ not_equal_text_text( _a_, _b_)→bool

Returns true if A and B are linguistically not equal (A != B).

Parameters:

- **a** ( _Text_)

- **b** ( _Text_)


Return type:

bool


---

_classmethod_ polyglot_data_to_text( _polyglot_data_)→Text

Get the text instance created from this polyglot data.

Parameters:

**polyglot\_data** ( _PolyglotTextData_)

Returns:

The text instance, or an empty text if the data is invalid.

Return type:

Text


---

_classmethod_ string_table_id_and_key_from_text( _text_)→(out_table_id=Name,out_key=str)orNone

Attempts to get the String Table ID and key used by the given text.

Parameters:

**text** ( _Text_)

Returns:

True if the String Table ID and key were found, false otherwise.

out\_table\_id (Name):

out\_key (str):

Return type:

tuple or None


---

_classmethod_ text_from_string_table( _table_id_, _key_)→Text

Attempts to create a text instance from a string table ID and key.
note: This exists to allow programmatic look-up of a string table entry from dynamic content - you should favor setting your string table reference on a text property or pin wherever possible as it is significantly more robust (see “Make Literal Text”).

Parameters:

- **table\_id** ( _Name_)

- **key** ( _str_)


Returns:

The found text, or a dummy text if the entry could not be found.

Return type:

Text


---

_classmethod_ text_is_culture_invariant( _text_)→bool

Returns true if text is culture invariant.

Parameters:

**text** ( _Text_)

Return type:

bool


---

_classmethod_ text_is_empty( _text_)→bool

Returns true if text is empty.

Parameters:

**text** ( _Text_)

Return type:

bool


---

_classmethod_ text_is_from_string_table( _text_)→bool

Returns true if the given text is referencing a string table.

Parameters:

**text** ( _Text_)

Return type:

bool


---

_classmethod_ text_is_transient( _text_)→bool

Returns true if text is transient.

Parameters:

**text** ( _Text_)

Return type:

bool


---

_classmethod_ text_to_lower( _text_)→Text

Transforms the text to lowercase in a culture correct way.
note: The returned instance is linked to the original and will be rebuilt if the active culture is changed.

Parameters:

**text** ( _Text_)

Return type:

Text


---

_classmethod_ text_to_upper( _text_)→Text

Transforms the text to uppercase in a culture correct way.
note: The returned instance is linked to the original and will be rebuilt if the active culture is changed.

Parameters:

**text** ( _Text_)

Return type:

Text


---

_classmethod_ text_trim_preceding( _text_)→Text

Removes whitespace characters from the front of the text.

Parameters:

**text** ( _Text_)

Return type:

Text


---

_classmethod_ text_trim_preceding_and_trailing( _text_)→Text

Removes whitespace characters from the front and end of the text.

Parameters:

**text** ( _Text_)

Return type:

Text


---

_classmethod_ text_trim_trailing( _text_)→Text

Removes trailing whitespace characters.

Parameters:

**text** ( _Text_)

Return type:

Text

### Table of Contents

- `unreal.TextLibrary`
  - `TextLibrary`
    - `TextLibrary.as_currency_base()`
    - `TextLibrary.as_currency_float()`
    - `TextLibrary.as_currency_integer()`
    - `TextLibrary.as_date_date_time()`
    - `TextLibrary.as_date_time_date_time()`
    - `TextLibrary.as_memory()`
    - `TextLibrary.as_percent_float()`
    - `TextLibrary.as_time_date_time()`
    - `TextLibrary.as_time_zone_date_date_time()`
    - `TextLibrary.as_time_zone_date_time_date_time()`
    - `TextLibrary.as_time_zone_time_date_time()`
    - `TextLibrary.as_timespan_timespan()`
    - `TextLibrary.conv_bool_to_text()`
    - `TextLibrary.conv_byte_to_text()`
    - `TextLibrary.conv_color_to_text()`
    - `TextLibrary.conv_double_to_text()`
    - `TextLibrary.conv_float_to_text()`
    - `TextLibrary.conv_int64_to_text()`
    - `TextLibrary.conv_int_to_text()`
    - `TextLibrary.conv_name_to_text()`
    - `TextLibrary.conv_object_to_text()`
    - `TextLibrary.conv_rotator_to_text()`
    - `TextLibrary.conv_string_to_text()`
    - `TextLibrary.conv_text_to_string()`
    - `TextLibrary.conv_transform_to_text()`
    - `TextLibrary.conv_vector2d_to_text()`
    - `TextLibrary.conv_vector_to_text()`
    - `TextLibrary.edit_text_property_source_string()`
    - `TextLibrary.equal_equal_ignore_case_text_text()`
    - `TextLibrary.equal_equal_text_text()`
    - `TextLibrary.find_text_in_live_table_advanced()`
    - `TextLibrary.find_text_in_localization_table()`
    - `TextLibrary.get_empty_text()`
    - `TextLibrary.get_text_id()`
    - `TextLibrary.get_text_source_string()`
    - `TextLibrary.is_polyglot_data_valid()`
    - `TextLibrary.make_invariant_text()`
    - `TextLibrary.not_equal_ignore_case_text_text()`
    - `TextLibrary.not_equal_text_text()`
    - `TextLibrary.polyglot_data_to_text()`
    - `TextLibrary.string_table_id_and_key_from_text()`
    - `TextLibrary.text_from_string_table()`
    - `TextLibrary.text_is_culture_invariant()`
    - `TextLibrary.text_is_empty()`
    - `TextLibrary.text_is_from_string_table()`
    - `TextLibrary.text_is_transient()`
    - `TextLibrary.text_to_lower()`
    - `TextLibrary.text_to_upper()`
    - `TextLibrary.text_trim_preceding()`
    - `TextLibrary.text_trim_preceding_and_trailing()`
    - `TextLibrary.text_trim_trailing()`