# unreal.ActionButtonStyle

```python
class unreal.ActionButtonStyle(button_style:ButtonStyle=Ellipsis, button_content_padding:type=(), combo_button_style:ComboButtonStyle=Ellipsis, has_down_arrow:bool=False, combo_button_content_padding:type=(), horizontal_content_alignment:HorizontalAlignment=Ellipsis, text_block_style:TextBlockStyle=Ellipsis, icon_brush:type=(), icon_color_and_opacity:type=(), icon_normal_padding:type=(), icon_pressed_padding:type=(), action_button_type:Name='None', icon_button_style:type=())
```


**Bases:** ``SlateWidgetStyle``


Represents the appearance of an SActionButton

**C++ Source:**

- **Module**: ToolWidgets

- **File**: ToolWidgetsSlateTypes.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `action_button_type` (Name): [Read-Write] The type to use for our SActionButton.

- `button_content_padding` (‘undefined’): [Read-Write] Spacing between button’s border and the content. Default uses ButtonStyle.

- `button_style` (ButtonStyle): [Read-Write] The style to use for our SButton.

- `combo_button_content_padding` (‘undefined’): [Read-Write] Spacing between button’s border and the content. Default uses ComboButtonStyle.

- `combo_button_style` (ComboButtonStyle): [Read-Write] The style to use for our SComboButton.

- `has_down_arrow` (bool): [Read-Write] Whether to show a down arrow for the combo button

- `horizontal_content_alignment` (HorizontalAlignment): [Read-Write] Horizontal Content alignment within the button.

- `icon_brush` (‘undefined’): [Read-Write] Icon Brush to use.

- `icon_button_style` (‘undefined’): [Read-Write] The style to use for our SButton when an icon is present. ButtonStyle used if not specified.

- `icon_color_and_opacity` (‘undefined’): [Read-Write] Icon Color/Tint, defaults is determined by ActionButtonType.

- `icon_normal_padding` (‘undefined’): [Read-Write] If set and the button’s icon is non-null, overrides the button style’s additional spacing between the button’s border and the content when not pressed.

- `icon_pressed_padding` (‘undefined’): [Read-Write] If set and the button’s icon is non-null, overrides the button style’s additional spacing between the button’s border and the content when pressed.

- `text_block_style` (TextBlockStyle): [Read-Write] The style to use for the button Text.



---

_property_ `action_button_type`: Name

[Read-Write] The type to use for our SActionButton.

**Type:**

( Name)


---

_property_ `button_content_padding`: type

[Read-Write] Spacing between button’s border and the content. Default uses ButtonStyle.

**Type:**

(‘undefined’)


---

_property_ `button_style`: ButtonStyle

[Read-Write] The style to use for our SButton.

**Type:**

( ButtonStyle)


---

_property_ `combo_button_content_padding`: type

[Read-Write] Spacing between button’s border and the content. Default uses ComboButtonStyle.

**Type:**

(‘undefined’)


---

_property_ `combo_button_style`: ComboButtonStyle

[Read-Write] The style to use for our SComboButton.

**Type:**

( ComboButtonStyle)


---

_property_ `has_down_arrow`: bool

[Read-Write] Whether to show a down arrow for the combo button

**Type:**

( bool)


---

_property_ `horizontal_content_alignment`: HorizontalAlignment

[Read-Write] Horizontal Content alignment within the button.

**Type:**

( HorizontalAlignment)


---

_property_ `icon_brush`: type

[Read-Write] Icon Brush to use.

**Type:**

(‘undefined’)


---

_property_ `icon_button_style`: type

[Read-Write] The style to use for our SButton when an icon is present. ButtonStyle used if not specified.

**Type:**

(‘undefined’)


---

_property_ `icon_color_and_opacity`: type

[Read-Write] Icon Color/Tint, defaults is determined by ActionButtonType.

**Type:**

(‘undefined’)


---

_property_ `icon_normal_padding`: type

[Read-Write] If set and the button’s icon is non-null, overrides the button style’s additional spacing between the button’s border and the content when not pressed.

**Type:**

(‘undefined’)


---

_property_ `icon_pressed_padding`: type

[Read-Write] If set and the button’s icon is non-null, overrides the button style’s additional spacing between the button’s border and the content when pressed.

**Type:**

(‘undefined’)


---

_property_ `text_block_style`: TextBlockStyle

[Read-Write] The style to use for the button Text.

**Type:**

( TextBlockStyle)

### Table of Contents

- `unreal.ActionButtonStyle`
  - `ActionButtonStyle`
    - `ActionButtonStyle.action_button_type`
    - `ActionButtonStyle.button_content_padding`
    - `ActionButtonStyle.button_style`
    - `ActionButtonStyle.combo_button_content_padding`
    - `ActionButtonStyle.combo_button_style`
    - `ActionButtonStyle.has_down_arrow`
    - `ActionButtonStyle.horizontal_content_alignment`
    - `ActionButtonStyle.icon_brush`
    - `ActionButtonStyle.icon_button_style`
    - `ActionButtonStyle.icon_color_and_opacity`
    - `ActionButtonStyle.icon_normal_padding`
    - `ActionButtonStyle.icon_pressed_padding`
    - `ActionButtonStyle.text_block_style`