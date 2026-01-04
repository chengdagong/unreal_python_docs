# unreal.DrawDebugLibrary

```python
class unreal.DrawDebugLibrary(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


A blueprint library of additional debug draw functions that unifies drawing between different debug drawing interfaces. Also includes a number of
helper functions and other convenience functions that are useful for debug drawing such as functions for recording histories.

General parameter structure for these functions is:

> Required Inputs, Style, bDepthTest, Settings

**C++ Source:**

- **Plugin**: DrawDebugLibrary

- **Module**: DrawDebugLibrary

- **File**: DrawDebugLibrary.h



---

_classmethod_ add_to_float_history_array( _out_values_, _new_value=0.000000_, _max_history_num=60_)→Array\ [float]

Convenience function that adds a float to the end of an array, popping values from the front once the max is reached

Parameters:

- **out\_values** ( _Array_ _\_ [_float_ _]_)

- **new\_value** ( _float_)

- **max\_history\_num** ( _int32_)


Returns:

out\_values (Array[float]):

Return type:

Array\ [float]


---

_classmethod_ add_to_vector_history_array( _out_values_, _new_value=[0.000000,0.000000,0.000000]_, _max_history_num=60_)→Array\ [Vector]

Convenience function that adds a vector to the end of an array, popping values from the front once the max is reached

Parameters:

- **out\_values** ( _Array_ _\_ [_Vector_ _]_)

- **new\_value** ( _Vector_)

- **max\_history\_num** ( _int32_)


Returns:

out\_values (Array[Vector]):

Return type:

Array\ [Vector]


---

_classmethod_ draw_debug_angle( _drawer_, _location_, _rotation_, _angle=0.000000_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _line_length=10.000000_, _angle_radius=5.000000_, _segments=17_)→None

Debug Draw an angle

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **angle** ( _float_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **line\_length** ( _float_)

- **angle\_radius** ( _float_)

- **segments** ( _int32_)



---

_classmethod_ draw_debug_arc( _drawer_, _location_, _rotation_, _angle=360.000000_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _radius=10.000000_, _segments=17_)→None

Debug Draw an arc around the XY axis

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **angle** ( _float_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **radius** ( _float_)

- **segments** ( _int32_)



---

_classmethod_ draw_debug_arrow( _drawer_, _start_location_, _end_location_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _settings=[False,False,5.000000,DrawDebugArrowHead.SIMPLE,True,False,5.000000,DrawDebugArrowHead.SIMPLE]_)→None

Debug Draw an arrow

Parameters:

- **drawer** ( _DebugDrawer_)

- **start\_location** ( _Vector_)

- **end\_location** ( _Vector_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **settings** ( _DrawDebugArrowSettings_)



---

_classmethod_ draw_debug_bone( _drawer_, _location_, _rotation_, _color=[0.000000,0.000000,0.025000,1.000000]_, _depth_test=True_, _radius=5.000000_, _segments=10_, _draw_transform=False_)→None

Debug Draw a bone

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **color** ( _LinearColor_)

- **depth\_test** ( _bool_)

- **radius** ( _float_)

- **segments** ( _int32_)

- **draw\_transform** ( _bool_)



---

_classmethod_ draw_debug_bone_link( _drawer_, _child_location_, _parent_location_, _parent_rotation_, _color=[0.000000,0.000000,0.025000,1.000000]_, _depth_test=True_, _radius=5.000000_)→None

Debug Draw a link between a child and parent bone

Parameters:

- **drawer** ( _DebugDrawer_)

- **child\_location** ( _Vector_)

- **parent\_location** ( _Vector_)

- **parent\_rotation** ( _Rotator_)

- **color** ( _LinearColor_)

- **depth\_test** ( _bool_)

- **radius** ( _float_)



---

_classmethod_ draw_debug_box( _drawer_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _half_extents=[10.000000,10.000000,10.000000]_)→None

Debug Draw an oriented box

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **half\_extents** ( _Vector_)



---

_classmethod_ draw_debug_camera( _drawer_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _scale=10.000000_, _fov_degees=30.000000_)→None

Debug draw a camera shape

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **scale** ( _float_)

- **fov\_degees** ( _float_)



---

_classmethod_ draw_debug_capsule( _drawer_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _radius=10.000000_, _half_length=10.000000_, _segments=8_)→None

Debug Draw a capsule

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **radius** ( _float_)

- **half\_length** ( _float_)

- **segments** ( _int32_)



---

_classmethod_ draw_debug_capsule_line( _drawer_, _start_location_, _end_location_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _radius=10.000000_, _segments=8_)→None

Debug Draw a capsule using the start and end location

Parameters:

- **drawer** ( _DebugDrawer_)

- **start\_location** ( _Vector_)

- **end\_location** ( _Vector_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **radius** ( _float_)

- **segments** ( _int32_)



---

_classmethod_ draw_debug_catmull_rom_spline( _drawer_, _points_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _monotonic=False_, _segments=15_)→None

Debug Draw a catmull rom spline

Parameters:

- **drawer** ( _DebugDrawer_)

- **points** ( _Array_ _\_ [_Vector_ _]_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **monotonic** ( _bool_)

- **segments** ( _int32_)



---

_classmethod_ draw_debug_catmull_rom_spline_end( _drawer_, _v0_, _v1_, _v2_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _monotonic=False_, _segments=15_)→None

Debug Draw the end section of a catmull rom spline

Parameters:

- **drawer** ( _DebugDrawer_)

- **v0** ( _Vector_)

- **v1** ( _Vector_)

- **v2** ( _Vector_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **monotonic** ( _bool_)

- **segments** ( _int32_)



---

_classmethod_ draw_debug_catmull_rom_spline_section( _drawer_, _v0_, _v1_, _v2_, _v3_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _monotonic=False_, _segments=15_)→None

Debug Draw a full segment of a catmull rom spline

Parameters:

- **drawer** ( _DebugDrawer_)

- **v0** ( _Vector_)

- **v1** ( _Vector_)

- **v2** ( _Vector_)

- **v3** ( _Vector_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **monotonic** ( _bool_)

- **segments** ( _int32_)



---

_classmethod_ draw_debug_catmull_rom_spline_start( _drawer_, _v0_, _v1_, _v2_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _monotonic=False_, _segments=15_)→None

Debug Draw the start section of a catmull rom spline

Parameters:

- **drawer** ( _DebugDrawer_)

- **v0** ( _Vector_)

- **v1** ( _Vector_)

- **v2** ( _Vector_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **monotonic** ( _bool_)

- **segments** ( _int32_)



---

_classmethod_ draw_debug_chair( _drawer_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _settings=[40.000000,40.000000,40.000000,10.000000]_)→None

Debug draw a basic chair shape

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **settings** ( _DrawDebugChairSettings_)



---

_classmethod_ draw_debug_circle( _drawer_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _radius=10.000000_, _segments=17_)→None

Debug Draw an circle around the XY axis

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **radius** ( _float_)

- **segments** ( _int32_)



---

_classmethod_ draw_debug_circle_arrow( _drawer_, _location_, _rotation_, _angle_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _radius=10.000000_, _length=20.000000_, _arrow_settings=[False,False,5.000000,DrawDebugArrowHead.SIMPLE,True,False,5.000000,DrawDebugArrowHead.SIMPLE]_)→None

Debug Draw an arrow coming off a circle at a given angle

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **angle** ( _float_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **radius** ( _float_)

- **length** ( _float_)

- **arrow\_settings** ( _DrawDebugArrowSettings_)



---

_classmethod_ draw_debug_circle_outline( _drawer_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _inner_radius=10.000000_, _outer_radius=15.000000_, _segments=17_)→None

Debug Draw the outline of a circle (two circles) around the XY axis

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **inner\_radius** ( _float_)

- **outer\_radius** ( _float_)

- **segments** ( _int32_)



---

_classmethod_ draw_debug_circle_tick( _drawer_, _location_, _rotation_, _angle_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _radius=10.000000_, _length=2.500000_, _inside=True_)→None

Debug Draw an tick on a circle at a given angle

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **angle** ( _float_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **radius** ( _float_)

- **length** ( _float_)

- **inside** ( _bool_)



---

_classmethod_ draw_debug_circle_ticks( _drawer_, _location_, _rotation_, _angles_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _radius=10.000000_, _length=5.000000_, _inside=True_)→None

Debug Draw ticks on a circle at the given angles

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **angles** ( _Array_ _\_ [_float_ _]_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **radius** ( _float_)

- **length** ( _float_)

- **inside** ( _bool_)



---

_classmethod_ draw_debug_cone( _drawer_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _length=20.000000_, _radius=10.000000_, _segments=9_)→None

Debug Draw a cone

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **length** ( _float_)

- **radius** ( _float_)

- **segments** ( _int32_)



---

_classmethod_ draw_debug_cross_locator( _drawer_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _radius=10.000000_)→None

Debug Draw an axis-aligned cross rotated by 45 degrees

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **radius** ( _float_)



---

_classmethod_ draw_debug_decagon( _drawer_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _radius=10.000000_)→None

Debug Draw a decagon on the XY axis

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **radius** ( _float_)



---

_classmethod_ draw_debug_diamond( _drawer_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _radius=10.000000_)→None

Debug Draw a diamond on the XY axis

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **radius** ( _float_)



---

_classmethod_ draw_debug_direction( _drawer_, _location_, _direction=[1.000000,0.000000,0.000000]_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _draw_arrow_length=100.000000_, _arrow_head_scale=1.000000_)→None

Debug Draw an arrow at the given location facing in the given direction

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **direction** ( _Vector_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **draw\_arrow\_length** ( _float_)

- **arrow\_head\_scale** ( _float_)



---

_classmethod_ draw_debug_door( _drawer_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _settings=[100.000000,200.000000,5.000000,90.000000,20.000000,3.000000,2.000000,True,True,True,True,40.000000]_)→None

Debug draw a basic door shape

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **settings** ( _DrawDebugDoorSettings_)



---

_classmethod_ draw_debug_event( _drawer_, _time_until_event_known_, _time_until_event_, _location_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _size=20.000000_)→None

Debug draw a phase-representation of an event at a location

Parameters:

- **drawer** ( _DebugDrawer_)

- **time\_until\_event\_known** ( _bool_)

- **time\_until\_event** ( _float_)

- **location** ( _Vector_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **size** ( _float_)



---

_classmethod_ draw_debug_flat_arrow( _drawer_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _length=20.000000_, _width=20.000000_)→None

Draws a flat 2d arrow motif

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **length** ( _float_)

- **width** ( _float_)



---

_classmethod_ draw_debug_frustum( _drawer_, _frustum_to_world_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_)→None

Debug Draw a Frustum

Parameters:

- **drawer** ( _DebugDrawer_)

- **frustum\_to\_world** ( _Matrix_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)



---

_classmethod_ draw_debug_graph( _drawer_, _location_, _rotation_, _xvalues_, _yvalues_, _xmin=0.000000_, _xmax=1.000000_, _ymin=0.000000_, _ymax=1.000000_, _xaxis_length=100.000000_, _yaxis_length=100.000000_, _text_line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _axes_line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _plot_line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _axes_settings=['',[10.000000,True,1.000000,1.000000,1.000000,0.000000],'','',[10.000000,True,1.000000,1.000000,1.000000,0.000000]]_)→None

Debug Draw a simple graph.

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **xvalues** ( _Array_ _\_ [_float_ _]_)

- **yvalues** ( _Array_ _\_ [_float_ _]_)

- **xmin** ( _float_)

- **xmax** ( _float_)

- **ymin** ( _float_)

- **ymax** ( _float_)

- **xaxis\_length** ( _float_)

- **yaxis\_length** ( _float_)

- **text\_line\_style** ( _DrawDebugLineStyle_)

- **axes\_line\_style** ( _DrawDebugLineStyle_)

- **plot\_line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **axes\_settings** ( _DrawDebugGraphAxesSettings_)



---

_classmethod_ draw_debug_graph_axes( _drawer_, _location_, _rotation_, _xaxis_length=100.000000_, _yaxis_length=100.000000_, _text_line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _axes_line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _axes_settings=['',[10.000000,True,1.000000,1.000000,1.000000,0.000000],'','',[10.000000,True,1.000000,1.000000,1.000000,0.000000]]_)→None

Debug Draw a simple graph axes.

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **xaxis\_length** ( _float_)

- **yaxis\_length** ( _float_)

- **text\_line\_style** ( _DrawDebugLineStyle_)

- **axes\_line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **axes\_settings** ( _DrawDebugGraphAxesSettings_)



---

_classmethod_ draw_debug_graph_legend( _drawer_, _location_, _rotation_, _legend_colors_, _legend_labels_, _xaxis_length=100.000000_, _yaxis_length=100.000000_, _text_line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _icon_line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _icon_size=2.500000_, _depth_test=True_, _legend_settings=[10.000000,True,1.000000,1.000000,1.000000,0.000000]_)→None

Debug Draw a simple graph legend.

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **legend\_colors** ( _Array_ _\_ [_LinearColor_ _]_)

- **legend\_labels** ( _Array_ _\_ [_str_ _]_)

- **xaxis\_length** ( _float_)

- **yaxis\_length** ( _float_)

- **text\_line\_style** ( _DrawDebugLineStyle_)

- **icon\_line\_style** ( _DrawDebugLineStyle_)

- **icon\_size** ( _float_)

- **depth\_test** ( _bool_)

- **legend\_settings** ( _DrawDebugStringSettings_)



---

_classmethod_ draw_debug_graph_line( _drawer_, _location_, _rotation_, _xvalues_, _yvalues_, _xmin=0.000000_, _xmax=1.000000_, _ymin=0.000000_, _ymax=1.000000_, _xaxis_length=100.000000_, _yaxis_length=100.000000_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_)→None

Debug Draw a line on a simple graph.

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **xvalues** ( _Array_ _\_ [_float_ _]_)

- **yvalues** ( _Array_ _\_ [_float_ _]_)

- **xmin** ( _float_)

- **xmax** ( _float_)

- **ymin** ( _float_)

- **ymax** ( _float_)

- **xaxis\_length** ( _float_)

- **yaxis\_length** ( _float_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)



---

_classmethod_ draw_debug_ground_target_arrow( _drawer_, _location_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _length=100.000000_, _arrow_head_size=20.000000_, _radius=10.000000_, _segments=17_)→None

Draws an arrow pointing down at the location surrounded by a circle

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **length** ( _float_)

- **arrow\_head\_size** ( _float_)

- **radius** ( _float_)

- **segments** ( _int32_)



---

_classmethod_ draw_debug_heptagon( _drawer_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _radius=10.000000_)→None

Debug Draw a heptagon on the XY axis

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **radius** ( _float_)



---

_classmethod_ draw_debug_hexagon( _drawer_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _radius=10.000000_)→None

Debug Draw a hexagon on the XY axis

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **radius** ( _float_)



---

_classmethod_ draw_debug_line( _drawer_, _start_location_, _end_location_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_)→None

Debug Draw a line

Parameters:

- **drawer** ( _DebugDrawer_)

- **start\_location** ( _Vector_)

- **end\_location** ( _Vector_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)



---

_classmethod_ draw_debug_line_style_color( _line_style_)→LinearColor

Get the color from a line style

Parameters:

**line\_style** ( _DrawDebugLineStyle_)

Return type:

LinearColor


---

_classmethod_ draw_debug_line_style_from_point_style( _point_style_)→DrawDebugLineStyle

Get a line style from a point style

Parameters:

**point\_style** ( _DrawDebugPointStyle_)

Return type:

DrawDebugLineStyle


---

_classmethod_ draw_debug_line_style_with_color( _line_style_, _color=[1.000000,0.000000,1.000000,1.000000]_)→DrawDebugLineStyle

Get a line style with the color changed

Parameters:

- **line\_style** ( _DrawDebugLineStyle_)

- **color** ( _LinearColor_)


Return type:

DrawDebugLineStyle


---

_classmethod_ draw_debug_line_style_with_color_no_opacity( _line_style_, _color=[1.000000,0.000000,1.000000,1.000000]_)→DrawDebugLineStyle

Get a line style with the color (excluding the opacity) changed

Parameters:

- **line\_style** ( _DrawDebugLineStyle_)

- **color** ( _LinearColor_)


Return type:

DrawDebugLineStyle


---

_classmethod_ draw_debug_line_style_with_thickness( _line_style_, _thickness=0.000000_)→DrawDebugLineStyle

Get a line style with the thickness changed

Parameters:

- **line\_style** ( _DrawDebugLineStyle_)

- **thickness** ( _float_)


Return type:

DrawDebugLineStyle


---

_classmethod_ draw_debug_line_style_with_type( _line_style_, _line_type=DrawDebugLineType.SOLID_)→DrawDebugLineStyle

Get a line style with the type changed

Parameters:

- **line\_style** ( _DrawDebugLineStyle_)

- **line\_type** ( _DrawDebugLineType_)


Return type:

DrawDebugLineStyle


---

_classmethod_ draw_debug_lines( _drawer_, _start_locations_, _end_locations_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_)→None

Debug Draw lines. These should be preferred over DrawDebugLine where possible as it will batch drawing when required such as when using the visual logger.

Parameters:

- **drawer** ( _DebugDrawer_)

- **start\_locations** ( _Array_ _\_ [_Vector_ _]_)

- **end\_locations** ( _Array_ _\_ [_Vector_ _]_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)



---

_classmethod_ draw_debug_location( _drawer_, _location_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _draw_radius=10.000000_, _segments=8_)→None

Debug Draw a sphere at the given location

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **draw\_radius** ( _float_)

- **segments** ( _int32_)



---

_classmethod_ draw_debug_locations( _drawer_, _locations_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _draw_radius=10.000000_, _segments=8_)→None

Debug Draw spheres at the given locations

Parameters:

- **drawer** ( _DebugDrawer_)

- **locations** ( _Array_ _\_ [_Vector_ _]_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **draw\_radius** ( _float_)

- **segments** ( _int32_)



---

_classmethod_ draw_debug_locator( _drawer_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _radius=10.000000_)→None

Debug Draw an axis-aligned cross

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **radius** ( _float_)



---

_classmethod_ draw_debug_mover_orientation( _drawer_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _forward_vector=[1.000000,0.000000,0.000000]_, _scale=30.000000_)→None

Draws a flat 2d motif representing mover position and rotation

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **forward\_vector** ( _Vector_)

- **scale** ( _float_)



---

_classmethod_ draw_debug_name( _drawer_, _name_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _settings=[10.000000,True,1.000000,1.000000,1.000000,0.000000]_)→None

Debug Draw a name

Parameters:

- **drawer** ( _DebugDrawer_)

- **name** ( _Name_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **settings** ( _DrawDebugStringSettings_)



---

_classmethod_ draw_debug_name_dimensions( _name_, _settings=[10.000000,True,1.000000,1.000000,1.000000,0.000000]_)→Vector

Get the dimensions of a draw debug name. Useful for aligning or centering text.

Parameters:

- **name** ( _Name_)

- **settings** ( _DrawDebugStringSettings_)


Return type:

Vector


---

_classmethod_ draw_debug_nonagon( _drawer_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _radius=10.000000_)→None

Debug Draw a nonagon on the XY axis

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **radius** ( _float_)



---

_classmethod_ draw_debug_octagon( _drawer_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _radius=10.000000_)→None

Debug Draw a octagon on the XY axis

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **radius** ( _float_)



---

_classmethod_ draw_debug_oriented_arrow( _drawer_, _location_, _rotation_, _length=100.000000_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _settings=[False,False,5.000000,DrawDebugArrowHead.SIMPLE,True,False,5.000000,DrawDebugArrowHead.SIMPLE]_)→None

Debug Draw an arrow with an orientation

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **length** ( _float_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **settings** ( _DrawDebugArrowSettings_)



---

_classmethod_ draw_debug_pentagon( _drawer_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _radius=10.000000_)→None

Debug Draw a pentagon on the XY axis

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **radius** ( _float_)



---

_classmethod_ draw_debug_point( _drawer_, _location_, _point_style=[0.000000,[1.000000,0.000000,1.000000,1.000000]]_, _depth_test=True_)→None

Debug Draw a point

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **point\_style** ( _DrawDebugPointStyle_)

- **depth\_test** ( _bool_)



---

_classmethod_ draw_debug_point_style_color( _point_style_)→LinearColor

Get the color from a point style

Parameters:

**point\_style** ( _DrawDebugPointStyle_)

Return type:

LinearColor


---

_classmethod_ draw_debug_point_style_from_line_style( _line_style_)→DrawDebugPointStyle

Get a point style from a line style

Parameters:

**line\_style** ( _DrawDebugLineStyle_)

Return type:

DrawDebugPointStyle


---

_classmethod_ draw_debug_points( _drawer_, _locations_, _point_style=[0.000000,[1.000000,0.000000,1.000000,1.000000]]_, _depth_test=True_)→None

Debug Draw points. These should be preferred over DrawDebugPoint where possible as it will batch drawing when required such as when using the visual logger.

Parameters:

- **drawer** ( _DebugDrawer_)

- **locations** ( _Array_ _\_ [_Vector_ _]_)

- **point\_style** ( _DrawDebugPointStyle_)

- **depth\_test** ( _bool_)



---

_classmethod_ draw_debug_pose( _drawer_, _bone_locations_, _bone_linear_velocities_, _relative_transform=[[0.000000,0.000000,0.000000],[-0.000000,0.000000,0.000000],[1.000000,1.000000,1.000000]]_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _draw_velocity_line_scale=1.000000_)→None

Debug Draw a pose made up of bone locations and velocities

Parameters:

- **drawer** ( _DebugDrawer_)

- **bone\_locations** ( _Array_ _\_ [_Vector_ _]_)

- **bone\_linear\_velocities** ( _Array_ _\_ [_Vector_ _]_)

- **relative\_transform** ( _Transform_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **draw\_velocity\_line\_scale** ( _float_)



---

_classmethod_ draw_debug_regular_polygon( _drawer_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _radius=10.000000_, _sides=11_)→None

Debug Draw a flat regular polygon on the XY axis

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **radius** ( _float_)

- **sides** ( _int32_)



---

_classmethod_ draw_debug_rotation( _drawer_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _draw_radius=10.000000_)→None

Draws a rotation

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **draw\_radius** ( _float_)



---

_classmethod_ draw_debug_simple_sphere( _drawer_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _radius=10.000000_, _segments=13_)→None

Debug Draw a simple sphere made up of three circles one of each axis

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **radius** ( _float_)

- **segments** ( _int32_)



---

_classmethod_ draw_debug_skeleton_from_skinned_mesh_component( _drawer_, _skinned_mesh_component_, _color=[0.000000,0.000000,0.025000,1.000000]_, _depth_test=False_, _settings=[False,1.000000,10,False,True,[1.000000,0.000000,0.000000,1.000000]]_)→None

Draws a skeleton from a skinned mesh component

Parameters:

- **drawer** ( _DebugDrawer_)

- **skinned\_mesh\_component** ( _SkinnedMeshComponent_)

- **color** ( _LinearColor_)

- **depth\_test** ( _bool_)

- **settings** ( _DrawDebugSkeletonSettings_)



---

_classmethod_ draw_debug_sphere( _drawer_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _radius=10.000000_, _segments=8_)→None

Debug Draw a sphere

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **radius** ( _float_)

- **segments** ( _int32_)



---

_classmethod_ draw_debug_square( _drawer_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _half_length=10.000000_)→None

Debug Draw a square on the XY axis

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **half\_length** ( _float_)



---

_classmethod_ draw_debug_square_base_pyramid( _drawer_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _length=20.000000_, _width=20.000000_)→None

Debug Draw a square base pyramid

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **length** ( _float_)

- **width** ( _float_)



---

_classmethod_ draw_debug_string( _drawer_, _string_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _settings=[10.000000,True,1.000000,1.000000,1.000000,0.000000]_)→None

Debug Draw a string. Will only render ASCII characters.

Parameters:

- **drawer** ( _DebugDrawer_)

- **string** ( _str_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **settings** ( _DrawDebugStringSettings_)



---

_classmethod_ draw_debug_string_dimensions( _string_, _settings=[10.000000,True,1.000000,1.000000,1.000000,0.000000]_)→Vector

Get the dimensions of a draw debug string. Useful for aligning or centering text.

Parameters:

- **string** ( _str_)

- **settings** ( _DrawDebugStringSettings_)


Return type:

Vector


---

_classmethod_ draw_debug_string_segment_num( _string_, _settings=[10.000000,True,1.000000,1.000000,1.000000,0.000000]_)→int32

Get the number of line segments required to draw debug string.

Parameters:

- **string** ( _str_)

- **settings** ( _DrawDebugStringSettings_)


Return type:

int32


---

_classmethod_ draw_debug_text( _drawer_, _text_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _settings=[10.000000,True,1.000000,1.000000,1.000000,0.000000]_)→None

Debug Draw some text. Will only render ASCII characters.

Parameters:

- **drawer** ( _DebugDrawer_)

- **text** ( _Text_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **settings** ( _DrawDebugStringSettings_)



---

_classmethod_ draw_debug_text_dimensions( _text_, _settings=[10.000000,True,1.000000,1.000000,1.000000,0.000000]_)→Vector

Get the dimensions of a draw debug text. Useful for aligning or centering text.

Parameters:

- **text** ( _Text_)

- **settings** ( _DrawDebugStringSettings_)


Return type:

Vector


---

_classmethod_ draw_debug_trajectory( _drawer_, _locations_, _directions_, _relative_transform=[[0.000000,0.000000,0.000000],[-0.000000,0.000000,0.000000],[1.000000,1.000000,1.000000]]_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _draw_arrow_length=100.000000_, _point_radius=5.000000_, _arrow_head_scale=1.000000_, _segments=9_, _vertical_offset=2.000000_)→None

Debug Draw a trajectory of locations and directions

Parameters:

- **drawer** ( _DebugDrawer_)

- **locations** ( _Array_ _\_ [_Vector_ _]_)

- **directions** ( _Array_ _\_ [_Vector_ _]_)

- **relative\_transform** ( _Transform_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **draw\_arrow\_length** ( _float_)

- **point\_radius** ( _float_)

- **arrow\_head\_scale** ( _float_)

- **segments** ( _int32_)

- **vertical\_offset** ( _float_)



---

_classmethod_ draw_debug_transform( _drawer_, _transform_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _draw_radius=10.000000_)→None

Debug Draw a set of axes at the given transform

Parameters:

- **drawer** ( _DebugDrawer_)

- **transform** ( _Transform_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **draw\_radius** ( _float_)



---

_classmethod_ draw_debug_transform_trajectory( _drawer_, _transform_trajectory_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _radius=5.000000_, _vertical_offset=2.000000_)→None

Debug Draw a transform trajectory

Parameters:

- **drawer** ( _DebugDrawer_)

- **transform\_trajectory** ( _TransformTrajectory_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **radius** ( _float_)

- **vertical\_offset** ( _float_)



---

_classmethod_ draw_debug_triangle( _drawer_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _radius=10.000000_)→None

Debug Draw a triangle on the XY axis

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **radius** ( _float_)



---

_classmethod_ draw_debug_triangular_base_pyramid( _drawer_, _location_, _rotation_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _length=20.000000_, _width=20.000000_)→None

Debug Draw a triangular base pyramid

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **length** ( _float_)

- **width** ( _float_)



---

_classmethod_ draw_debug_velocities( _drawer_, _locations_, _velocities_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _draw_velocity_line_scale=1.000000_)→None

Debug draw velocities

Parameters:

- **drawer** ( _DebugDrawer_)

- **locations** ( _Array_ _\_ [_Vector_ _]_)

- **velocities** ( _Array_ _\_ [_Vector_ _]_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **draw\_velocity\_line\_scale** ( _float_)



---

_classmethod_ draw_debug_velocity( _drawer_, _location_, _velocity_, _line_style=[DrawDebugLineType.SOLID,0.000000,[1.000000,0.000000,1.000000,1.000000],2.500000,1.000000,1.000000]_, _depth_test=True_, _draw_velocity_line_scale=1.000000_)→None

Debug Draw a line at the given location scaled by the given velocity

Parameters:

- **drawer** ( _DebugDrawer_)

- **location** ( _Vector_)

- **velocity** ( _Vector_)

- **line\_style** ( _DrawDebugLineStyle_)

- **depth\_test** ( _bool_)

- **draw\_velocity\_line\_scale** ( _float_)



---

_classmethod_ get_default_bone_color()→LinearColor

Gets the default debug draw bone color

Return type:

LinearColor


---

_classmethod_ get_default_bone_radius()→float

Gets the default debug draw bone radius

Return type:

float


---

_classmethod_ make_debug_drawer( _object_)→DebugDrawer

Make a debug debugger from the current “Self” object

Parameters:

**object** ( _Object_)

Return type:

DebugDrawer


---

_classmethod_ make_draw_debug_line_style_from_color( _color=[1.000000,0.000000,1.000000,1.000000]_)→DrawDebugLineStyle

Make a line style from a color

Parameters:

**color** ( _LinearColor_)

Return type:

DrawDebugLineStyle


---

_classmethod_ make_draw_debug_point_style_from_color( _color=[1.000000,0.000000,1.000000,1.000000]_)→DrawDebugPointStyle

Make a point style from a color

Parameters:

**color** ( _LinearColor_)

Return type:

DrawDebugPointStyle


---

_classmethod_ make_linearly_spaced_float_array( _start=0.000000_, _stop=1.000000_, _num=10_)→Array\ [float]

Convenience function for making an array of linearly spaced float values

Parameters:

- **start** ( _float_)

- **stop** ( _float_)

- **num** ( _int32_)


Returns:

out\_values (Array[float]):

Return type:

Array\ [float]


---

_classmethod_ make_merged_debug_drawer( _debug_drawers_)→DebugDrawer

Make a debug drawer by merging multiple other debug drawers of different types

Parameters:

**debug\_drawers** ( _Array_ _\_ [_DebugDrawer_ _]_)

Return type:

DebugDrawer


---

_classmethod_ make_null_debug_drawer()→DebugDrawer

Make a null debug drawer which ignores draw commands

Return type:

DebugDrawer


---

_classmethod_ make_object_debug_drawer( _object_)→DebugDrawer

Make a debug drawer for a UObject

Parameters:

**object** ( _Object_)

Return type:

DebugDrawer


---

_classmethod_ make_visual_logger_debug_drawer( _object_, _category='LogDrawDebugLibrary'_, _verbosity=DrawDebugLogVerbosity.DISPLAY_, _draw_to_scene=True_, _draw_to_scene_while_recording=True_)→DebugDrawer

Make a debug drawer for the Visual Logger from the current “Self” object

Parameters:

- **object** ( _Object_)

- **category** ( _Name_)

- **verbosity** ( _DrawDebugLogVerbosity_)

- **draw\_to\_scene** ( _bool_)

- **draw\_to\_scene\_while\_recording** ( _bool_)


Return type:

DebugDrawer


---

_classmethod_ make_visual_logger_debug_drawer_from_object( _object_, _category='LogDrawDebugLibrary'_, _verbosity=DrawDebugLogVerbosity.DISPLAY_, _draw_to_scene=True_, _draw_to_scene_while_recording=True_)→DebugDrawer

Make a debug drawer for the Visual Logger

Parameters:

- **object** ( _Object_)

- **category** ( _Name_)

- **verbosity** ( _DrawDebugLogVerbosity_)

- **draw\_to\_scene** ( _bool_)

- **draw\_to\_scene\_while\_recording** ( _bool_)


Return type:

DebugDrawer


---

_classmethod_ visual_logger_draw_name( _drawer_, _name_, _location_, _color=[1.000000,0.000000,1.000000,1.000000]_)→None

Debug Draw a name to the visual logger. Will do nothing if not using a VisualLoggerDrawer. Will not display on-screen during recording.

Parameters:

- **drawer** ( _DebugDrawer_)

- **name** ( _Name_)

- **location** ( _Vector_)

- **color** ( _LinearColor_)



---

_classmethod_ visual_logger_draw_string( _drawer_, _string_, _location_, _color=[1.000000,0.000000,1.000000,1.000000]_)→None

Debug Draw a string to the visual logger. Will do nothing if not using a VisualLoggerDrawer. Will not display on-screen during recording.

Parameters:

- **drawer** ( _DebugDrawer_)

- **string** ( _str_)

- **location** ( _Vector_)

- **color** ( _LinearColor_)



---

_classmethod_ visual_logger_draw_text( _drawer_, _text_, _location_, _color=[1.000000,0.000000,1.000000,1.000000]_)→None

Debug Draw some text to the visual logger. Will do nothing if not using a VisualLoggerDrawer. Will not display on-screen during recording.

Parameters:

- **drawer** ( _DebugDrawer_)

- **text** ( _Text_)

- **location** ( _Vector_)

- **color** ( _LinearColor_)



---

_classmethod_ visual_logger_log_string( _drawer_, _string_, _color=[1.000000,0.000000,1.000000,1.000000]_)→None

Log a string to the visual logger. Only does anything with a VisualLoggerDebugDrawer.

Parameters:

- **drawer** ( _DebugDrawer_)

- **string** ( _str_)

- **color** ( _LinearColor_)



---

_classmethod_ visual_logger_log_text( _drawer_, _text_, _color=[1.000000,0.000000,1.000000,1.000000]_)→None

Log some text to the visual logger. Only does anything with a VisualLoggerDebugDrawer.

Parameters:

- **drawer** ( _DebugDrawer_)

- **text** ( _Text_)

- **color** ( _LinearColor_)


### Table of Contents

- `unreal.DrawDebugLibrary`
  - `DrawDebugLibrary`
    - `DrawDebugLibrary.add_to_float_history_array()`
    - `DrawDebugLibrary.add_to_vector_history_array()`
    - `DrawDebugLibrary.draw_debug_angle()`
    - `DrawDebugLibrary.draw_debug_arc()`
    - `DrawDebugLibrary.draw_debug_arrow()`
    - `DrawDebugLibrary.draw_debug_bone()`
    - `DrawDebugLibrary.draw_debug_bone_link()`
    - `DrawDebugLibrary.draw_debug_box()`
    - `DrawDebugLibrary.draw_debug_camera()`
    - `DrawDebugLibrary.draw_debug_capsule()`
    - `DrawDebugLibrary.draw_debug_capsule_line()`
    - `DrawDebugLibrary.draw_debug_catmull_rom_spline()`
    - `DrawDebugLibrary.draw_debug_catmull_rom_spline_end()`
    - `DrawDebugLibrary.draw_debug_catmull_rom_spline_section()`
    - `DrawDebugLibrary.draw_debug_catmull_rom_spline_start()`
    - `DrawDebugLibrary.draw_debug_chair()`
    - `DrawDebugLibrary.draw_debug_circle()`
    - `DrawDebugLibrary.draw_debug_circle_arrow()`
    - `DrawDebugLibrary.draw_debug_circle_outline()`
    - `DrawDebugLibrary.draw_debug_circle_tick()`
    - `DrawDebugLibrary.draw_debug_circle_ticks()`
    - `DrawDebugLibrary.draw_debug_cone()`
    - `DrawDebugLibrary.draw_debug_cross_locator()`
    - `DrawDebugLibrary.draw_debug_decagon()`
    - `DrawDebugLibrary.draw_debug_diamond()`
    - `DrawDebugLibrary.draw_debug_direction()`
    - `DrawDebugLibrary.draw_debug_door()`
    - `DrawDebugLibrary.draw_debug_event()`
    - `DrawDebugLibrary.draw_debug_flat_arrow()`
    - `DrawDebugLibrary.draw_debug_frustum()`
    - `DrawDebugLibrary.draw_debug_graph()`
    - `DrawDebugLibrary.draw_debug_graph_axes()`
    - `DrawDebugLibrary.draw_debug_graph_legend()`
    - `DrawDebugLibrary.draw_debug_graph_line()`
    - `DrawDebugLibrary.draw_debug_ground_target_arrow()`
    - `DrawDebugLibrary.draw_debug_heptagon()`
    - `DrawDebugLibrary.draw_debug_hexagon()`
    - `DrawDebugLibrary.draw_debug_line()`
    - `DrawDebugLibrary.draw_debug_line_style_color()`
    - `DrawDebugLibrary.draw_debug_line_style_from_point_style()`
    - `DrawDebugLibrary.draw_debug_line_style_with_color()`
    - `DrawDebugLibrary.draw_debug_line_style_with_color_no_opacity()`
    - `DrawDebugLibrary.draw_debug_line_style_with_thickness()`
    - `DrawDebugLibrary.draw_debug_line_style_with_type()`
    - `DrawDebugLibrary.draw_debug_lines()`
    - `DrawDebugLibrary.draw_debug_location()`
    - `DrawDebugLibrary.draw_debug_locations()`
    - `DrawDebugLibrary.draw_debug_locator()`
    - `DrawDebugLibrary.draw_debug_mover_orientation()`
    - `DrawDebugLibrary.draw_debug_name()`
    - `DrawDebugLibrary.draw_debug_name_dimensions()`
    - `DrawDebugLibrary.draw_debug_nonagon()`
    - `DrawDebugLibrary.draw_debug_octagon()`
    - `DrawDebugLibrary.draw_debug_oriented_arrow()`
    - `DrawDebugLibrary.draw_debug_pentagon()`
    - `DrawDebugLibrary.draw_debug_point()`
    - `DrawDebugLibrary.draw_debug_point_style_color()`
    - `DrawDebugLibrary.draw_debug_point_style_from_line_style()`
    - `DrawDebugLibrary.draw_debug_points()`
    - `DrawDebugLibrary.draw_debug_pose()`
    - `DrawDebugLibrary.draw_debug_regular_polygon()`
    - `DrawDebugLibrary.draw_debug_rotation()`
    - `DrawDebugLibrary.draw_debug_simple_sphere()`
    - `DrawDebugLibrary.draw_debug_skeleton_from_skinned_mesh_component()`
    - `DrawDebugLibrary.draw_debug_sphere()`
    - `DrawDebugLibrary.draw_debug_square()`
    - `DrawDebugLibrary.draw_debug_square_base_pyramid()`
    - `DrawDebugLibrary.draw_debug_string()`
    - `DrawDebugLibrary.draw_debug_string_dimensions()`
    - `DrawDebugLibrary.draw_debug_string_segment_num()`
    - `DrawDebugLibrary.draw_debug_text()`
    - `DrawDebugLibrary.draw_debug_text_dimensions()`
    - `DrawDebugLibrary.draw_debug_trajectory()`
    - `DrawDebugLibrary.draw_debug_transform()`
    - `DrawDebugLibrary.draw_debug_transform_trajectory()`
    - `DrawDebugLibrary.draw_debug_triangle()`
    - `DrawDebugLibrary.draw_debug_triangular_base_pyramid()`
    - `DrawDebugLibrary.draw_debug_velocities()`
    - `DrawDebugLibrary.draw_debug_velocity()`
    - `DrawDebugLibrary.get_default_bone_color()`
    - `DrawDebugLibrary.get_default_bone_radius()`
    - `DrawDebugLibrary.make_debug_drawer()`
    - `DrawDebugLibrary.make_draw_debug_line_style_from_color()`
    - `DrawDebugLibrary.make_draw_debug_point_style_from_color()`
    - `DrawDebugLibrary.make_linearly_spaced_float_array()`
    - `DrawDebugLibrary.make_merged_debug_drawer()`
    - `DrawDebugLibrary.make_null_debug_drawer()`
    - `DrawDebugLibrary.make_object_debug_drawer()`
    - `DrawDebugLibrary.make_visual_logger_debug_drawer()`
    - `DrawDebugLibrary.make_visual_logger_debug_drawer_from_object()`
    - `DrawDebugLibrary.visual_logger_draw_name()`
    - `DrawDebugLibrary.visual_logger_draw_string()`
    - `DrawDebugLibrary.visual_logger_draw_text()`
    - `DrawDebugLibrary.visual_logger_log_string()`
    - `DrawDebugLibrary.visual_logger_log_text()`