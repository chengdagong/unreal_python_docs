# unreal.Text3DStyleBase

```python
class unreal.Text3DStyleBase(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


Text3D rich text format styles

**C++ Source:**

- **Plugin**: Text3D

- **Module**: Text3D

- **File**: Text3DStyleBase.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `font` (Font): [Read-Write] Text font defines the style of rendered characters

- `font_size` (float): [Read-Write] Text font size to render and scale each character

- `font_typeface` (Name): [Read-Write] Text font face, subset within font like bold, italic, regular

- `front_color` (LinearColor): [Read-Write] Text front color

- `override_font` (bool): [Read-Write] Behavior for the font rule of this style

- `override_font_size` (bool): [Read-Write] Behavior for the size rule of this style

- `override_front_color` (bool): [Read-Write] Behavior for the front color rule of this style

- `style_name` (Name): [Read-Write] Style name used in text



---

**get_font**() → `Font`

Get Font

Return type:

Font


---

**get_font_size**() → `float`

Get Font Size

Return type:

float


---

**get_font_typeface**() → `Name`

Get Font Typeface

Return type:

Name


---

**get_front_color**() → `LinearColor`

Get Front Color

Return type:

LinearColor


---

**get_override_font**() → `bool`

Get Override Font

Return type:

bool


---

**get_override_font_size**() → `bool`

Get Override Font Size

Return type:

bool


---

**get_override_front_color**() → `bool`

Get Override Front Color

Return type:

bool


---

**get_style_name**() → `Name`

Get Style Name

Return type:

Name


---

**set_font**( _font_) → `None`

Set Font

Parameters:

**font** ( _Font_)


---

**set_font_size**( _size_) → `None`

Set Font Size

Parameters:

**size** ( _float_)


---

**set_font_typeface**( _typeface_) → `None`

Set Font Typeface

Parameters:

**typeface** ( _Name_)


---

**set_front_color**( _color_) → `None`

Set Front Color

Parameters:

**color** ( _LinearColor_)


---

**set_override_font**( _override_) → `None`

Set Override Font

Parameters:

**override** ( _bool_)


---

**set_override_font_size**( _override_) → `None`

Set Override Font Size

Parameters:

**override** ( _bool_)


---

**set_override_front_color**( _override_) → `None`

Set Override Front Color

Parameters:

**override** ( _bool_)


---

**set_style_name**( _name_) → `None`

Set Style Name

Parameters:

**name** ( _Name_)

### Table of Contents

- `unreal.Text3DStyleBase`
  - `Text3DStyleBase`
    - `Text3DStyleBase.get_font()`
    - `Text3DStyleBase.get_font_size()`
    - `Text3DStyleBase.get_font_typeface()`
    - `Text3DStyleBase.get_front_color()`
    - `Text3DStyleBase.get_override_font()`
    - `Text3DStyleBase.get_override_font_size()`
    - `Text3DStyleBase.get_override_front_color()`
    - `Text3DStyleBase.get_style_name()`
    - `Text3DStyleBase.set_font()`
    - `Text3DStyleBase.set_font_size()`
    - `Text3DStyleBase.set_font_typeface()`
    - `Text3DStyleBase.set_front_color()`
    - `Text3DStyleBase.set_override_font()`
    - `Text3DStyleBase.set_override_font_size()`
    - `Text3DStyleBase.set_override_front_color()`
    - `Text3DStyleBase.set_style_name()`