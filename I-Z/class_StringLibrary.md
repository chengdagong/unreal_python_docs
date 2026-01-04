# unreal.StringLibrary

```python
class unreal.StringLibrary(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


Kismet String Library

**C++ Source:**

- **Module**: Engine

- **File**: KismetStringLibrary.h



---

_classmethod_ build_string_bool( _append_to_, _prefix_, _bool_, _suffix_)→str

Converts a boolean->string, creating a new string in the form AppendTo+Prefix+InBool+Suffix

Parameters:

- **append\_to** ( _str_) – An existing string to use as the start of the conversion string

- **prefix** ( _str_) – A string to use as a prefix, after the AppendTo string

- **bool** ( _bool_) – The bool value to convert. Will add “true” or “false” to the conversion string

- **suffix** ( _str_) – A suffix to append to the end of the conversion string


Returns:

A new string built from the passed parameters

Return type:

str


---

_classmethod_ build_string_color( _append_to_, _prefix_, _color_, _suffix_)→str

Converts a color->string, creating a new string in the form AppendTo+Prefix+InColor+Suffix

Parameters:

- **append\_to** ( _str_) – An existing string to use as the start of the conversion string

- **prefix** ( _str_) – A string to use as a prefix, after the AppendTo string

- **color** ( _LinearColor_) – The linear color value to convert. Uses the standard ToString conversion

- **suffix** ( _str_) – A suffix to append to the end of the conversion string


Returns:

A new string built from the passed parameters

Return type:

str


---

_classmethod_ build_string_double( _append_to_, _prefix_, _double_, _suffix_)→str

Converts a double->string, create a new string in the form AppendTo+Prefix+InDouble+Suffix

Parameters:

- **append\_to** ( _str_) – An existing string to use as the start of the conversion string

- **prefix** ( _str_) – A string to use as a prefix, after the AppendTo string

- **double** ( _double_) – The double value to convert

- **suffix** ( _str_) – A suffix to append to the end of the conversion string


Returns:

A new string built from the passed parameters

Return type:

str


---

_classmethod_ build_string_float( _append_to:str_, _prefix:str_, _double:float_, _suffix:str_)→str

deprecated: ‘build\_string\_float’ was renamed to ‘build\_string\_double’.


---

_classmethod_ build_string_int( _append_to_, _prefix_, _int_, _suffix_)→str

Converts a int->string, creating a new string in the form AppendTo+Prefix+InInt+Suffix

Parameters:

- **append\_to** ( _str_) – An existing string to use as the start of the conversion string

- **prefix** ( _str_) – A string to use as a prefix, after the AppendTo string

- **int** ( _int32_) – The int value to convert

- **suffix** ( _str_) – A suffix to append to the end of the conversion string


Returns:

A new string built from the passed parameters

Return type:

str


---

_classmethod_ build_string_int_vector( _append_to_, _prefix_, _int_vector2_, _suffix_)→str

Converts an IntVector->string, creating a new string in the form AppendTo+Prefix+InIntVector+Suffix

Parameters:

- **append\_to** ( _str_) – An existing string to use as the start of the conversion string

- **prefix** ( _str_) – A string to use as a prefix, after the AppendTo string

- **int\_vector2** ( _IntVector_)

- **suffix** ( _str_) – A suffix to append to the end of the conversion string


Returns:

A new string built from the passed parameters

Return type:

str


---

_classmethod_ build_string_int_vector2( _append_to_, _prefix_, _int_vector_, _suffix_)→str

Converts an IntVector2->string, creating a new string in the form AppendTo+Prefix+InIntVector+Suffix

Parameters:

- **append\_to** ( _str_) – An existing string to use as the start of the conversion string

- **prefix** ( _str_) – A string to use as a prefix, after the AppendTo string

- **int\_vector** ( _IntVector2_) – The intVector2 value to convert. Uses the standard FVector::ToString conversion

- **suffix** ( _str_) – A suffix to append to the end of the conversion string


Returns:

A new string built from the passed parameters

Return type:

str


---

_classmethod_ build_string_name( _append_to_, _prefix_, _name_, _suffix_)→str

Converts a color->string, creating a new string in the form AppendTo+Prefix+InName+Suffix

Parameters:

- **append\_to** ( _str_) – An existing string to use as the start of the conversion string

- **prefix** ( _str_) – A string to use as a prefix, after the AppendTo string

- **name** ( _Name_) – The name value to convert

- **suffix** ( _str_) – A suffix to append to the end of the conversion string


Returns:

A new string built from the passed parameters

Return type:

str


---

_classmethod_ build_string_object( _append_to_, _prefix_, _obj_, _suffix_)→str

Converts a object->string, creating a new string in the form AppendTo+Prefix+object name+Suffix

Parameters:

- **append\_to** ( _str_) – An existing string to use as the start of the conversion string

- **prefix** ( _str_) – A string to use as a prefix, after the AppendTo string

- **obj** ( _Object_) – The object to convert. Will insert the name of the object into the conversion string

- **suffix** ( _str_) – A suffix to append to the end of the conversion string


Returns:

A new string built from the passed parameters

Return type:

str


---

_classmethod_ build_string_rotator( _append_to_, _prefix_, _rot_, _suffix_)→str

Converts a rotator->string, creating a new string in the form AppendTo+Prefix+InRot+Suffix

Parameters:

- **append\_to** ( _str_) – An existing string to use as the start of the conversion string

- **prefix** ( _str_) – A string to use as a prefix, after the AppendTo string

- **rot** ( _Rotator_) – The rotator value to convert. Uses the standard ToString conversion

- **suffix** ( _str_) – A suffix to append to the end of the conversion string


Returns:

A new string built from the passed parameters

Return type:

str


---

_classmethod_ build_string_vector( _append_to_, _prefix_, _vector_, _suffix_)→str

Converts a vector->string, creating a new string in the form AppendTo+Prefix+InVector+Suffix

Parameters:

- **append\_to** ( _str_) – An existing string to use as the start of the conversion string

- **prefix** ( _str_) – A string to use as a prefix, after the AppendTo string

- **vector** ( _Vector_) – The vector value to convert. Uses the standard FVector::ToString conversion

- **suffix** ( _str_) – A suffix to append to the end of the conversion string


Returns:

A new string built from the passed parameters

Return type:

str


---

_classmethod_ build_string_vector2d( _append_to_, _prefix_, _vector2d_, _suffix_)→str

Converts a vector2d->string, creating a new string in the form AppendTo+Prefix+InVector2d+Suffix

Parameters:

- **append\_to** ( _str_) – An existing string to use as the start of the conversion string

- **prefix** ( _str_) – A string to use as a prefix, after the AppendTo string

- **vector2d** ( _Vector2D_) – The vector2d value to convert. Uses the standard FVector2D::ToString conversion

- **suffix** ( _str_) – A suffix to append to the end of the conversion string


Returns:

A new string built from the passed parameters

Return type:

str


---

_classmethod_ concat_str_str( _a_, _b_)→str

Concatenates two strings together to make a new string

Parameters:

- **a** ( _str_) – The original string

- **b** ( _str_) – The string to append to A


Returns:

A new string which is the concatenation of A+B

Return type:

str


---

_classmethod_ contains( _search_in_, _substring_, _use_case=False_, _search_from_end=False_)→bool

Returns whether this string contains the specified substring.

Parameters:

- **search\_in** ( _str_)

- **substring** ( _str_)

- **use\_case** ( _bool_)

- **search\_from\_end** ( _bool_)


Returns:

Returns whether the string contains the substring

Return type:

bool


---

_classmethod_ conv_bool_to_string( _bool_)→str

Converts a boolean value to a string, either ‘true’ or ‘false’

Parameters:

**bool** ( _bool_)

Return type:

str


---

_classmethod_ conv_box_center_and_extents_to_string( _box_)→str

Converts a FBox value to a string of its Center and Extents values.

Parameters:

**box** ( _Box_)

Return type:

str


---

_classmethod_ conv_box_to_string( _box_)→str

Converts a FBox value to a string

Parameters:

**box** ( _Box_)

Return type:

str


---

_classmethod_ conv_byte_to_string( _byte_)→str

Converts a byte value to a string

Parameters:

**byte** ( _uint8_)

Return type:

str


---

_classmethod_ conv_color_to_string( _color_)→str

Converts a linear color value to a string, in the form ‘(R=,G=,B=,A=)’

Parameters:

**color** ( _LinearColor_)

Return type:

str


---

_classmethod_ conv_double_to_string( _double_)→str

Converts a double value to a string

Parameters:

**double** ( _double_)

Return type:

str


---

_classmethod_ conv_float_to_string( _double:float_)→str

deprecated: ‘conv\_float\_to\_string’ was renamed to ‘conv\_double\_to\_string’.


---

_classmethod_ conv_input_device_id_to_string( _device_id_)→str

Converts a InputDeviceId value to a string

Parameters:

**device\_id** ( _InputDeviceId_)

Return type:

str


---

_classmethod_ conv_int64_to_string( _int_)→str

Converts an 64-bit integer value to a string

Parameters:

**int** ( _int64_)

Return type:

str


---

_classmethod_ conv_int_point_to_string( _int_point_)→str

Converts an IntPoint value to a string, in the form ‘X= Y=’

Parameters:

**int\_point** ( _IntPoint_)

Return type:

str


---

_classmethod_ conv_int_to_string( _int_)→str

Converts an integer value to a string

Parameters:

**int** ( _int32_)

Return type:

str


---

_classmethod_ conv_int_vector2_to_string( _int_vec2_)→str

Converts an IntVector2 value to a string, in the form ‘X= Y=’

Parameters:

**int\_vec2** ( _IntVector2_)

Return type:

str


---

_classmethod_ conv_int_vector_to_string( _int_vec_)→str

Converts an IntVector value to a string, in the form ‘X= Y= Z=’

Parameters:

**int\_vec** ( _IntVector_)

Return type:

str


---

_classmethod_ conv_matrix_to_string( _matrix_)→str

Converts a name value to a string

Parameters:

**matrix** ( _Matrix_)

Return type:

str


---

_classmethod_ conv_name_to_string( _name_)→str

Converts a name value to a string

Parameters:

**name** ( _Name_)

Return type:

str


---

_classmethod_ conv_object_to_string( _obj_)→str

Converts a UObject value to a string by calling the object’s GetName method

Parameters:

**obj** ( _Object_)

Return type:

str


---

_classmethod_ conv_platform_user_id_to_string( _platform_user_id_)→str

Converts a PlatformUserId value to a string

Parameters:

**platform\_user\_id** ( _PlatformUserId_)

Return type:

str


---

_classmethod_ conv_rotator_to_string( _rot_)→str

Converts a rotator value to a string, in the form ‘P= Y= R=’

Parameters:

**rot** ( _Rotator_)

Return type:

str

_classmethod_ conv\_string\_to\_color( _string)->(out\_converted\_color=LinearColor_, _out\_is\_valid=bool_)

Convert String Back To Color. IsValid indicates whether or not the string could be successfully converted.

Parameters:

**string** ( _str_)

Returns:

out\_converted\_color (LinearColor):

out\_is\_valid (bool):

Return type:

tuple


---

_classmethod_ conv_string_to_double( _string_)→double

Converts a string to a double value

Parameters:

**string** ( _str_)

Return type:

double


---

_classmethod_ conv_string_to_float( _string:str_)→float

deprecated: ‘conv\_string\_to\_float’ was renamed to ‘conv\_string\_to\_double’.


---

_classmethod_ conv_string_to_int( _string_)→int32

Converts a string to a int value

Parameters:

**string** ( _str_)

Return type:

int32


---

_classmethod_ conv_string_to_int64( _string_)→int64

Converts a string to a int value

Parameters:

**string** ( _str_)

Return type:

int64


---

_classmethod_ conv_string_to_name( _string_)→Name

Converts a string to a name value

Parameters:

**string** ( _str_)

Return type:

Name

_classmethod_ conv\_string\_to\_rotator( _string)->(out\_converted\_rotator=Rotator_, _out\_is\_valid=bool_)

Convert String Back To Rotator. IsValid indicates whether or not the string could be successfully converted.

Parameters:

**string** ( _str_)

Returns:

out\_converted\_rotator (Rotator):

out\_is\_valid (bool):

Return type:

tuple

_classmethod_ conv\_string\_to\_vector( _string)->(out\_converted\_vector=Vector_, _out\_is\_valid=bool_)

Convert String Back To Vector. IsValid indicates whether or not the string could be successfully converted.

Parameters:

**string** ( _str_)

Returns:

out\_converted\_vector (Vector):

out\_is\_valid (bool):

Return type:

tuple

_classmethod_ conv\_string\_to\_vector2d( _string)->(out\_converted\_vector2d=Vector2D_, _out\_is\_valid=bool_)

Convert String Back To Vector2D. IsValid indicates whether or not the string could be successfully converted.

Parameters:

**string** ( _str_)

Returns:

out\_converted\_vector2d (Vector2D):

out\_is\_valid (bool):

Return type:

tuple

_classmethod_ conv\_string\_to\_vector3f( _string)->(out\_converted\_vector=Vector3f_, _out\_is\_valid=bool_)

Convert String Back To Float Vector. IsValid indicates whether or not the string could be successfully converted.

Parameters:

**string** ( _str_)

Returns:

out\_converted\_vector (Vector3f):

out\_is\_valid (bool):

Return type:

tuple


---

_classmethod_ conv_transform_to_string( _trans_)→str

Converts a transform value to a string, in the form ‘Translation: X= Y= Z= Rotation: P= Y= R= Scale: X= Y= Z=’

Parameters:

**trans** ( _Transform_)

Return type:

str


---

_classmethod_ conv_vector2d_to_string( _vec_)→str

Converts a vector2d value to a string, in the form ‘X= Y=’

Parameters:

**vec** ( _Vector2D_)

Return type:

str


---

_classmethod_ conv_vector3f_to_string( _vec_)→str

Converts a float vector value to a string, in the form ‘X= Y= Z=’

Parameters:

**vec** ( _Vector3f_)

Return type:

str


---

_classmethod_ conv_vector_to_string( _vec_)→str

Converts a vector value to a string, in the form ‘X= Y= Z=’

Parameters:

**vec** ( _Vector_)

Return type:

str

_classmethod_ cull\_array( _source\_string)->(int32,array=Array[str]_)

Takes an array of strings and removes any zero length entries.

Parameters:

**source\_string** ( _str_)

Returns:

The number of elements left in InArray

array (Array[str]): The array to cull

Return type:

Array\ [str]


---

_classmethod_ diff_string( _first_, _second_)→str

Returns a string describing the LCS difference between two strings, First and Second.
This function is editor only because it is expensive for large strings. Examples:

(“A”, “”) -> “- [ 0001 | ] A”
(“”, “”) -\> “”
(“The quick brown fox”, “The quick red fox”) -> “~ [ 0001 | 0001 ]

> The quick brown fox
>
> The quick red fox”

The numbers between the [], separated by |, are the line numbers in the First and Second string at
which the difference occurs. Preceding the line number information is a symbol identifying the type
of difference: A tilde (~) indicates a modification, a minus (-) indicates a removal from First, and
a plus (+) indicates an addition to second.

Parameters:

- **first** ( _str_) – The string to treat as basis

- **second** ( _str_) – The string to treat as change


Returns:

the LCS difference between the First and Second string

Return type:

str


---

_classmethod_ ends_with( _source_string_, _suffix_, _search_case=SearchCase.IGNORE_CASE_)→bool

Test whether this string ends with given string.

Parameters:

- **source\_string** ( _str_)

- **suffix** ( _str_)

- **search\_case** ( _SearchCase_) – Indicates whether the search is case sensitive or not ( defaults to ESearchCase::IgnoreCase )


Returns:

true if this string ends with specified text, false otherwise

Return type:

bool


---

_classmethod_ equal_equal_str_str( _a_, _b_)→bool

Test if the input strings are equal (A == B)

Parameters:

- **a** ( _str_) – The string to compare against

- **b** ( _str_) – The string to compare


Returns:

True if the strings are equal, false otherwise

Return type:

bool


---

_classmethod_ equal_equal_stri_stri( _a_, _b_)→bool

Test if the input strings are equal (A == B), ignoring case

Parameters:

- **a** ( _str_) – The string to compare against

- **b** ( _str_) – The string to compare


Returns:

True if the strings are equal, false otherwise

Return type:

bool


---

_classmethod_ find_substring( _search_in_, _substring_, _use_case=False_, _search_from_end=False_, _start_position=-1_)→int32

Finds the starting index of a substring in the a specified string

Parameters:

- **search\_in** ( _str_) – The string to search within

- **substring** ( _str_) – The string to look for in the SearchIn string

- **use\_case** ( _bool_) – Whether or not to be case-sensitive

- **search\_from\_end** ( _bool_) – Whether or not to start the search from the end of the string instead of the beginning

- **start\_position** ( _int32_) – The position to start the search from


Returns:

The index (starting from 0 if bSearchFromEnd is false) of the first occurence of the substring

Return type:

int32


---

_classmethod_ get_character_array_from_string( _source_string_)→Array\ [str]

Returns an array that contains one entry for each character in SourceString

Parameters:

**source\_string** ( _str_) – The string to break apart into characters

Returns:

An array containing one entry for each character in SourceString

Return type:

Array\ [str]


---

_classmethod_ get_character_as_number( _source_string_, _index=0_)→int32

Gets a single character from the string (as an integer)

Parameters:

- **source\_string** ( _str_) – The string to convert

- **index** ( _int32_) – Location of the character whose value is required


Returns:

The integer value of the character or 0 if index is out of range

Return type:

int32


---

_classmethod_ get_substring( _source_string_, _start_index=0_, _length=1_)→str

Returns a substring from the string starting at the specified position

Parameters:

- **source\_string** ( _str_) – The string to get the substring from

- **start\_index** ( _int32_) – The location in SourceString to use as the start of the substring

- **length** ( _int32_) – The length of the requested substring


Returns:

The requested substring

Return type:

str


---

_classmethod_ is_empty( _string_)→bool

Returns true if the string is empty

Parameters:

**string** ( _str_) – The string to check

Returns:

Whether or not the string is empty

Return type:

bool


---

_classmethod_ is_numeric( _source_string_)→bool

- Checks if a string contains only numeric characters


Parameters:

**source\_string** ( _str_) – The string to check \*

Returns:

true if the string only contains numeric characters

Return type:

bool


---

_classmethod_ join_string_array( _source_array_, _separator=''_)→str

Concatenates an array of strings into a single string.

Parameters:

- **source\_array** ( _Array_ _\_ [_str_ _]_) – The array of strings to concatenate.

- **separator** ( _str_) – The string used to separate each element.


Returns:

The final, joined, separated string.

Return type:

str


---

_classmethod_ left( _source_string_, _count_)→str

Returns the left most given number of characters

Parameters:

- **source\_string** ( _str_)

- **count** ( _int32_)


Return type:

str


---

_classmethod_ left_chop( _source_string_, _count_)→str

Returns the left most characters from the string chopping the given number of characters from the end

Parameters:

- **source\_string** ( _str_)

- **count** ( _int32_)


Return type:

str


---

_classmethod_ left_pad( _source_string_, _ch_count_)→str

- Pad the left of this string for a specified number of characters


Parameters:

- **source\_string** ( _str_) – The string to pad \*

- **ch\_count** ( _int32_) – Amount of padding required \*


Returns:

The padded string

Return type:

str


---

_classmethod_ len( _s_)→int32

Returns the number of characters in the string

Parameters:

**s** ( _str_)

Returns:

The number of chars in the string

Return type:

int32


---

_classmethod_ matches_wildcard( _source_string_, _wildcard_, _search_case=SearchCase.IGNORE_CASE_)→bool

Searches this string for a given wild card
warning: This is a simple, SLOW routine. Use with caution

Parameters:

- **source\_string** ( _str_)

- **wildcard** ( _str_) – \*?-type wildcard

- **search\_case** ( _SearchCase_) – Indicates whether the search is case sensitive or not ( defaults to ESearchCase::IgnoreCase )


Returns:

true if this string matches the \*?-type wildcard given.

Return type:

bool


---

_classmethod_ mid( _source_string_, _start_, _count_)→str

Returns the substring from Start position for Count characters.

Parameters:

- **source\_string** ( _str_)

- **start** ( _int32_)

- **count** ( _int32_)


Return type:

str


---

_classmethod_ not_equal_str_str( _a_, _b_)→bool

Test if the input string are not equal (A != B)

Parameters:

- **a** ( _str_) – The string to compare against

- **b** ( _str_) – The string to compare


Returns:

Returns true if the input strings are not equal, false if they are equal

Return type:

bool


---

_classmethod_ not_equal_stri_stri( _a_, _b_)→bool

Test if the input string are not equal (A != B), ignoring case differences

Parameters:

- **a** ( _str_) – The string to compare against

- **b** ( _str_) – The string to compare


Returns:

Returns true if the input strings are not equal, false if they are equal

Return type:

bool


---

_classmethod_ parse_into_array( _source_string_, _delimiter=''_, _cull_empty_strings=True_)→Array\ [str]

Gets an array of strings from a source string divided up by a separator and empty strings can optionally be culled.

Parameters:

- **source\_string** ( _str_) – The string to chop up

- **delimiter** ( _str_) – The string to delimit on

- **cull\_empty\_strings** ( _bool_) – = true - Cull (true) empty strings or add them to the array (false)


Returns:

The array of string that have been separated

Return type:

Array\ [str]


---

_classmethod_ replace( _source_string_, _from__, _to_, _search_case=SearchCase.IGNORE_CASE_)→str

Replace all occurrences of a substring in this string

Parameters:

- **source\_string** ( _str_)

- **from** ( _str_) – substring to replace

- **to** ( _str_) – substring to replace From with

- **search\_case** ( _SearchCase_) – Indicates whether the search is case sensitive or not ( defaults to ESearchCase::IgnoreCase )


Returns:

a copy of this string with the replacement made

Return type:

str

_classmethod_ replace\_inline( _source\_string_, _search\_text_, _replacement\_text_, _search\_case=SearchCase.IGNORE\_CASE)->(int32_, _source\_string=str_)

Replace all occurrences of SearchText with ReplacementText in this string.

Parameters:

- **source\_string** ( _str_)

- **search\_text** ( _str_) – the text that should be removed from this string

- **replacement\_text** ( _str_) – the text to insert in its place

- **search\_case** ( _SearchCase_) – Indicates whether the search is case sensitive or not ( defaults to ESearchCase::IgnoreCase )


Returns:

the number of occurrences of SearchText that were replaced.

source\_string (str):

Return type:

str


---

_classmethod_ reverse( _source_string_)→str

Returns a copy of this string, with the characters in reverse order

Parameters:

**source\_string** ( _str_)

Return type:

str


---

_classmethod_ right( _source_string_, _count_)→str

Returns the string to the right of the specified location, counting back from the right (end of the word).

Parameters:

- **source\_string** ( _str_)

- **count** ( _int32_)


Return type:

str


---

_classmethod_ right_chop( _source_string_, _count_)→str

Returns the string to the right of the specified location, counting forward from the left (from the beginning of the word).

Parameters:

- **source\_string** ( _str_)

- **count** ( _int32_)


Return type:

str


---

_classmethod_ right_pad( _source_string_, _ch_count_)→str

- Pad the right of this string for a specified number of characters


Parameters:

- **source\_string** ( _str_) – The string to pad \*

- **ch\_count** ( _int32_) – Amount of padding required \*


Returns:

The padded string

Return type:

str


---

_classmethod_ split( _source_string_, _str_, _search_case=SearchCase.IGNORE_CASE_, _search_dir=SearchDir.FROM_START_)→(left_s=str,right_s=str)orNone

Splits this string at given string position case sensitive.

Parameters:

- **source\_string** ( _str_)

- **str** ( _str_) – The string to search and split at

- **search\_case** ( _SearchCase_) – Indicates whether the search is case sensitive or not ( defaults to ESearchCase::IgnoreCase )

- **search\_dir** ( _SearchDir_) – Indicates whether the search starts at the begining or at the end ( defaults to ESearchDir::FromStart )


Returns:

true if string is split, otherwise false

left\_s (str): out the string to the left of InStr, not updated if return is false

right\_s (str): out the string to the right of InStr, not updated if return is false

Return type:

tuple or None


---

_classmethod_ starts_with( _source_string_, _prefix_, _search_case=SearchCase.IGNORE_CASE_)→bool

Test whether this string starts with given string.

Parameters:

- **source\_string** ( _str_)

- **prefix** ( _str_)

- **search\_case** ( _SearchCase_) – Indicates whether the search is case sensitive or not ( defaults to ESearchCase::IgnoreCase )


Returns:

true if this string begins with specified text, false otherwise

Return type:

bool


---

_classmethod_ time_seconds_to_string( _seconds_)→str

Convert a number of seconds into minutes:seconds.milliseconds format string (including leading zeroes)

Parameters:

**seconds** ( _float_)

Returns:

A new string built from the seconds parameter

Return type:

str


---

_classmethod_ to_lower( _source_string_)→str

Returns a string converted to Lower case

Parameters:

**source\_string** ( _str_) – The string to convert

Returns:

The string in lower case

Return type:

str


---

_classmethod_ to_upper( _source_string_)→str

Returns a string converted to Upper case

Parameters:

**source\_string** ( _str_) – The string to convert

Returns:

The string in upper case

Return type:

str


---

_classmethod_ trim( _source_string_)→str

Removes whitespace characters from the front of this string.

Parameters:

**source\_string** ( _str_)

Return type:

str


---

_classmethod_ trim_trailing( _source_string_)→str

Removes trailing whitespace characters

Parameters:

**source\_string** ( _str_)

Return type:

str

### Table of Contents

- `unreal.StringLibrary`
  - `StringLibrary`
    - `StringLibrary.build_string_bool()`
    - `StringLibrary.build_string_color()`
    - `StringLibrary.build_string_double()`
    - `StringLibrary.build_string_float()`
    - `StringLibrary.build_string_int()`
    - `StringLibrary.build_string_int_vector()`
    - `StringLibrary.build_string_int_vector2()`
    - `StringLibrary.build_string_name()`
    - `StringLibrary.build_string_object()`
    - `StringLibrary.build_string_rotator()`
    - `StringLibrary.build_string_vector()`
    - `StringLibrary.build_string_vector2d()`
    - `StringLibrary.concat_str_str()`
    - `StringLibrary.contains()`
    - `StringLibrary.conv_bool_to_string()`
    - `StringLibrary.conv_box_center_and_extents_to_string()`
    - `StringLibrary.conv_box_to_string()`
    - `StringLibrary.conv_byte_to_string()`
    - `StringLibrary.conv_color_to_string()`
    - `StringLibrary.conv_double_to_string()`
    - `StringLibrary.conv_float_to_string()`
    - `StringLibrary.conv_input_device_id_to_string()`
    - `StringLibrary.conv_int64_to_string()`
    - `StringLibrary.conv_int_point_to_string()`
    - `StringLibrary.conv_int_to_string()`
    - `StringLibrary.conv_int_vector2_to_string()`
    - `StringLibrary.conv_int_vector_to_string()`
    - `StringLibrary.conv_matrix_to_string()`
    - `StringLibrary.conv_name_to_string()`
    - `StringLibrary.conv_object_to_string()`
    - `StringLibrary.conv_platform_user_id_to_string()`
    - `StringLibrary.conv_rotator_to_string()`
    - `StringLibrary.conv_string_to_color()`
    - `StringLibrary.conv_string_to_double()`
    - `StringLibrary.conv_string_to_float()`
    - `StringLibrary.conv_string_to_int()`
    - `StringLibrary.conv_string_to_int64()`
    - `StringLibrary.conv_string_to_name()`
    - `StringLibrary.conv_string_to_rotator()`
    - `StringLibrary.conv_string_to_vector()`
    - `StringLibrary.conv_string_to_vector2d()`
    - `StringLibrary.conv_string_to_vector3f()`
    - `StringLibrary.conv_transform_to_string()`
    - `StringLibrary.conv_vector2d_to_string()`
    - `StringLibrary.conv_vector3f_to_string()`
    - `StringLibrary.conv_vector_to_string()`
    - `StringLibrary.cull_array()`
    - `StringLibrary.diff_string()`
    - `StringLibrary.ends_with()`
    - `StringLibrary.equal_equal_str_str()`
    - `StringLibrary.equal_equal_stri_stri()`
    - `StringLibrary.find_substring()`
    - `StringLibrary.get_character_array_from_string()`
    - `StringLibrary.get_character_as_number()`
    - `StringLibrary.get_substring()`
    - `StringLibrary.is_empty()`
    - `StringLibrary.is_numeric()`
    - `StringLibrary.join_string_array()`
    - `StringLibrary.left()`
    - `StringLibrary.left_chop()`
    - `StringLibrary.left_pad()`
    - `StringLibrary.len()`
    - `StringLibrary.matches_wildcard()`
    - `StringLibrary.mid()`
    - `StringLibrary.not_equal_str_str()`
    - `StringLibrary.not_equal_stri_stri()`
    - `StringLibrary.parse_into_array()`
    - `StringLibrary.replace()`
    - `StringLibrary.replace_inline()`
    - `StringLibrary.reverse()`
    - `StringLibrary.right()`
    - `StringLibrary.right_chop()`
    - `StringLibrary.right_pad()`
    - `StringLibrary.split()`
    - `StringLibrary.starts_with()`
    - `StringLibrary.time_seconds_to_string()`
    - `StringLibrary.to_lower()`
    - `StringLibrary.to_upper()`
    - `StringLibrary.trim()`
    - `StringLibrary.trim_trailing()`