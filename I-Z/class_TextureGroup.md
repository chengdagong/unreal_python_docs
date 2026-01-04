# unreal.TextureGroup

```python
class unreal.TextureGroup
```


**Bases:** ``EnumBase``


warning:: if this is changed: update BaseEngine.ini [SystemSettings] you might have to update the update Game’s DefaultEngine.ini [SystemSettings] order and actual name can never change (order is important!) TEXTUREGROUP\_Cinematic: should be used for Cinematics which will be baked out and want to have the highest settings

**C++ Source:**

- **Module**: Engine

- **File**: TextureDefines.h


TEXTUREGROUP\_16\_BIT\_DATA _: TextureGroup_ _=Ellipsis_

16 bit data stored in textures

**Type:**

33

TEXTUREGROUP\_8\_BIT\_DATA _: TextureGroup_ _=Ellipsis_

8 bit data stored in textures

**Type:**

32

TEXTUREGROUP\_BOKEH _: TextureGroup_ _=Ellipsis_

Using this TextureGroup triggers special mip map generation code only useful for the BokehDOF post process.

**Type:**

26

TEXTUREGROUP\_CHARACTER _: TextureGroup_ _=Ellipsis_

3

TEXTUREGROUP\_CHARACTER\_NORMAL\_MAP _: TextureGroup_ _=Ellipsis_

4

TEXTUREGROUP\_CHARACTER\_SPECULAR _: TextureGroup_ _=Ellipsis_

5

TEXTUREGROUP\_CINEMATIC _: TextureGroup_ _=Ellipsis_

12

TEXTUREGROUP\_COLOR\_LOOKUP\_TABLE _: TextureGroup_ _=Ellipsis_

No compression, no mips.

**Type:**

23

TEXTUREGROUP\_EFFECTS _: TextureGroup_ _=Ellipsis_

13

TEXTUREGROUP\_EFFECTS\_NOT\_FILTERED _: TextureGroup_ _=Ellipsis_

14

TEXTUREGROUP\_HIERARCHICAL\_LOD _: TextureGroup_ _=Ellipsis_

Hierarchical LOD generated textures

**Type:**

29

TEXTUREGROUP\_IES\_LIGHT\_PROFILE _: TextureGroup_ _=Ellipsis_

No compression, created on import of a .IES file.

**Type:**

27

TEXTUREGROUP\_IMPOSTOR _: TextureGroup_ _=Ellipsis_

Impostor Color Textures

**Type:**

30

TEXTUREGROUP\_IMPOSTOR\_NORMAL\_DEPTH _: TextureGroup_ _=Ellipsis_

Impostor Normal and Depth, use default compression

**Type:**

31

TEXTUREGROUP\_LIGHTMAP _: TextureGroup_ _=Ellipsis_

17

TEXTUREGROUP\_MOBILE\_FLATTENED _: TextureGroup_ _=Ellipsis_

19

TEXTUREGROUP\_PIXELS2D _: TextureGroup_ _=Ellipsis_

Non-filtered, useful for 2D rendering.

**Type:**

28

TEXTUREGROUP\_PROC\_BUILDING\_FACE _: TextureGroup_ _=Ellipsis_

Obsolete - kept for backwards compatibility.

**Type:**

20

TEXTUREGROUP\_PROC\_BUILDING\_LIGHT\_MAP _: TextureGroup_ _=Ellipsis_

Obsolete - kept for backwards compatibility.

**Type:**

21

TEXTUREGROUP\_PROJECT01 _: TextureGroup_ _=Ellipsis_

Project specific group, rename in Engine.ini, [EnumRemap] TEXTUREGROUP\_Project\*\*.DisplayName=My Fun Group

**Type:**

34

TEXTUREGROUP\_PROJECT02 _: TextureGroup_ _=Ellipsis_

35

TEXTUREGROUP\_PROJECT03 _: TextureGroup_ _=Ellipsis_

36

TEXTUREGROUP\_PROJECT04 _: TextureGroup_ _=Ellipsis_

37

TEXTUREGROUP\_PROJECT05 _: TextureGroup_ _=Ellipsis_

38

TEXTUREGROUP\_PROJECT06 _: TextureGroup_ _=Ellipsis_

39

TEXTUREGROUP\_PROJECT07 _: TextureGroup_ _=Ellipsis_

40

TEXTUREGROUP\_PROJECT08 _: TextureGroup_ _=Ellipsis_

41

TEXTUREGROUP\_PROJECT09 _: TextureGroup_ _=Ellipsis_

42

TEXTUREGROUP\_PROJECT10 _: TextureGroup_ _=Ellipsis_

43

TEXTUREGROUP\_PROJECT11 _: TextureGroup_ _=Ellipsis_

44

TEXTUREGROUP\_PROJECT12 _: TextureGroup_ _=Ellipsis_

45

TEXTUREGROUP\_PROJECT13 _: TextureGroup_ _=Ellipsis_

46

TEXTUREGROUP\_PROJECT14 _: TextureGroup_ _=Ellipsis_

47

TEXTUREGROUP\_PROJECT15 _: TextureGroup_ _=Ellipsis_

48

TEXTUREGROUP\_PROJECT16 _: TextureGroup_ _=Ellipsis_

49

TEXTUREGROUP\_PROJECT17 _: TextureGroup_ _=Ellipsis_

50

TEXTUREGROUP\_PROJECT18 _: TextureGroup_ _=Ellipsis_

51

TEXTUREGROUP\_PROJECT19 _: TextureGroup_ _=Ellipsis_

52

TEXTUREGROUP\_PROJECT20 _: TextureGroup_ _=Ellipsis_

53

TEXTUREGROUP\_PROJECT21 _: TextureGroup_ _=Ellipsis_

54

TEXTUREGROUP\_PROJECT22 _: TextureGroup_ _=Ellipsis_

55

TEXTUREGROUP\_PROJECT23 _: TextureGroup_ _=Ellipsis_

56

TEXTUREGROUP\_PROJECT24 _: TextureGroup_ _=Ellipsis_

57

TEXTUREGROUP\_PROJECT25 _: TextureGroup_ _=Ellipsis_

58

TEXTUREGROUP\_PROJECT26 _: TextureGroup_ _=Ellipsis_

59

TEXTUREGROUP\_PROJECT27 _: TextureGroup_ _=Ellipsis_

60

TEXTUREGROUP\_PROJECT28 _: TextureGroup_ _=Ellipsis_

61

TEXTUREGROUP\_PROJECT29 _: TextureGroup_ _=Ellipsis_

62

TEXTUREGROUP\_PROJECT30 _: TextureGroup_ _=Ellipsis_

63

TEXTUREGROUP\_PROJECT31 _: TextureGroup_ _=Ellipsis_

64

TEXTUREGROUP\_PROJECT32 _: TextureGroup_ _=Ellipsis_

65

TEXTUREGROUP\_PROJECT33 _: TextureGroup_ _=Ellipsis_

66

TEXTUREGROUP\_PROJECT34 _: TextureGroup_ _=Ellipsis_

67

TEXTUREGROUP\_PROJECT35 _: TextureGroup_ _=Ellipsis_

68

TEXTUREGROUP\_PROJECT36 _: TextureGroup_ _=Ellipsis_

69

TEXTUREGROUP\_PROJECT37 _: TextureGroup_ _=Ellipsis_

70

TEXTUREGROUP\_PROJECT38 _: TextureGroup_ _=Ellipsis_

71

TEXTUREGROUP\_PROJECT39 _: TextureGroup_ _=Ellipsis_

72

TEXTUREGROUP\_PROJECT40 _: TextureGroup_ _=Ellipsis_

73

TEXTUREGROUP\_PROJECT41 _: TextureGroup_ _=Ellipsis_

74

TEXTUREGROUP\_PROJECT42 _: TextureGroup_ _=Ellipsis_

75

TEXTUREGROUP\_PROJECT43 _: TextureGroup_ _=Ellipsis_

76

TEXTUREGROUP\_PROJECT44 _: TextureGroup_ _=Ellipsis_

77

TEXTUREGROUP\_PROJECT45 _: TextureGroup_ _=Ellipsis_

78

TEXTUREGROUP\_PROJECT46 _: TextureGroup_ _=Ellipsis_

79

TEXTUREGROUP\_PROJECT47 _: TextureGroup_ _=Ellipsis_

80

TEXTUREGROUP\_PROJECT48 _: TextureGroup_ _=Ellipsis_

81

TEXTUREGROUP\_RENDER\_TARGET _: TextureGroup_ _=Ellipsis_

18

TEXTUREGROUP\_SHADOWMAP _: TextureGroup_ _=Ellipsis_

22

TEXTUREGROUP\_SKYBOX _: TextureGroup_ _=Ellipsis_

15

TEXTUREGROUP\_TERRAIN\_HEIGHTMAP _: TextureGroup_ _=Ellipsis_

24

TEXTUREGROUP\_TERRAIN\_WEIGHTMAP _: TextureGroup_ _=Ellipsis_

25

TEXTUREGROUP\_UI _: TextureGroup_ _=Ellipsis_

16

TEXTUREGROUP\_VEHICLE _: TextureGroup_ _=Ellipsis_

9

TEXTUREGROUP\_VEHICLE\_NORMAL\_MAP _: TextureGroup_ _=Ellipsis_

10

TEXTUREGROUP\_VEHICLE\_SPECULAR _: TextureGroup_ _=Ellipsis_

11

TEXTUREGROUP\_WEAPON _: TextureGroup_ _=Ellipsis_

6

TEXTUREGROUP\_WEAPON\_NORMAL\_MAP _: TextureGroup_ _=Ellipsis_

7

TEXTUREGROUP\_WEAPON\_SPECULAR _: TextureGroup_ _=Ellipsis_

8

TEXTUREGROUP\_WORLD _: TextureGroup_ _=Ellipsis_

0

TEXTUREGROUP\_WORLD\_NORMAL\_MAP _: TextureGroup_ _=Ellipsis_

1

TEXTUREGROUP\_WORLD\_SPECULAR _: TextureGroup_ _=Ellipsis_

2

### Table of Contents

- `unreal.TextureGroup`
  - `TextureGroup`
    - `TextureGroup.TEXTUREGROUP_16_BIT_DATA`
    - `TextureGroup.TEXTUREGROUP_8_BIT_DATA`
    - `TextureGroup.TEXTUREGROUP_BOKEH`
    - `TextureGroup.TEXTUREGROUP_CHARACTER`
    - `TextureGroup.TEXTUREGROUP_CHARACTER_NORMAL_MAP`
    - `TextureGroup.TEXTUREGROUP_CHARACTER_SPECULAR`
    - `TextureGroup.TEXTUREGROUP_CINEMATIC`
    - `TextureGroup.TEXTUREGROUP_COLOR_LOOKUP_TABLE`
    - `TextureGroup.TEXTUREGROUP_EFFECTS`
    - `TextureGroup.TEXTUREGROUP_EFFECTS_NOT_FILTERED`
    - `TextureGroup.TEXTUREGROUP_HIERARCHICAL_LOD`
    - `TextureGroup.TEXTUREGROUP_IES_LIGHT_PROFILE`
    - `TextureGroup.TEXTUREGROUP_IMPOSTOR`
    - `TextureGroup.TEXTUREGROUP_IMPOSTOR_NORMAL_DEPTH`
    - `TextureGroup.TEXTUREGROUP_LIGHTMAP`
    - `TextureGroup.TEXTUREGROUP_MOBILE_FLATTENED`
    - `TextureGroup.TEXTUREGROUP_PIXELS2D`
    - `TextureGroup.TEXTUREGROUP_PROC_BUILDING_FACE`
    - `TextureGroup.TEXTUREGROUP_PROC_BUILDING_LIGHT_MAP`
    - `TextureGroup.TEXTUREGROUP_PROJECT01`
    - `TextureGroup.TEXTUREGROUP_PROJECT02`
    - `TextureGroup.TEXTUREGROUP_PROJECT03`
    - `TextureGroup.TEXTUREGROUP_PROJECT04`
    - `TextureGroup.TEXTUREGROUP_PROJECT05`
    - `TextureGroup.TEXTUREGROUP_PROJECT06`
    - `TextureGroup.TEXTUREGROUP_PROJECT07`
    - `TextureGroup.TEXTUREGROUP_PROJECT08`
    - `TextureGroup.TEXTUREGROUP_PROJECT09`
    - `TextureGroup.TEXTUREGROUP_PROJECT10`
    - `TextureGroup.TEXTUREGROUP_PROJECT11`
    - `TextureGroup.TEXTUREGROUP_PROJECT12`
    - `TextureGroup.TEXTUREGROUP_PROJECT13`
    - `TextureGroup.TEXTUREGROUP_PROJECT14`
    - `TextureGroup.TEXTUREGROUP_PROJECT15`
    - `TextureGroup.TEXTUREGROUP_PROJECT16`
    - `TextureGroup.TEXTUREGROUP_PROJECT17`
    - `TextureGroup.TEXTUREGROUP_PROJECT18`
    - `TextureGroup.TEXTUREGROUP_PROJECT19`
    - `TextureGroup.TEXTUREGROUP_PROJECT20`
    - `TextureGroup.TEXTUREGROUP_PROJECT21`
    - `TextureGroup.TEXTUREGROUP_PROJECT22`
    - `TextureGroup.TEXTUREGROUP_PROJECT23`
    - `TextureGroup.TEXTUREGROUP_PROJECT24`
    - `TextureGroup.TEXTUREGROUP_PROJECT25`
    - `TextureGroup.TEXTUREGROUP_PROJECT26`
    - `TextureGroup.TEXTUREGROUP_PROJECT27`
    - `TextureGroup.TEXTUREGROUP_PROJECT28`
    - `TextureGroup.TEXTUREGROUP_PROJECT29`
    - `TextureGroup.TEXTUREGROUP_PROJECT30`
    - `TextureGroup.TEXTUREGROUP_PROJECT31`
    - `TextureGroup.TEXTUREGROUP_PROJECT32`
    - `TextureGroup.TEXTUREGROUP_PROJECT33`
    - `TextureGroup.TEXTUREGROUP_PROJECT34`
    - `TextureGroup.TEXTUREGROUP_PROJECT35`
    - `TextureGroup.TEXTUREGROUP_PROJECT36`
    - `TextureGroup.TEXTUREGROUP_PROJECT37`
    - `TextureGroup.TEXTUREGROUP_PROJECT38`
    - `TextureGroup.TEXTUREGROUP_PROJECT39`
    - `TextureGroup.TEXTUREGROUP_PROJECT40`
    - `TextureGroup.TEXTUREGROUP_PROJECT41`
    - `TextureGroup.TEXTUREGROUP_PROJECT42`
    - `TextureGroup.TEXTUREGROUP_PROJECT43`
    - `TextureGroup.TEXTUREGROUP_PROJECT44`
    - `TextureGroup.TEXTUREGROUP_PROJECT45`
    - `TextureGroup.TEXTUREGROUP_PROJECT46`
    - `TextureGroup.TEXTUREGROUP_PROJECT47`
    - `TextureGroup.TEXTUREGROUP_PROJECT48`
    - `TextureGroup.TEXTUREGROUP_RENDER_TARGET`
    - `TextureGroup.TEXTUREGROUP_SHADOWMAP`
    - `TextureGroup.TEXTUREGROUP_SKYBOX`
    - `TextureGroup.TEXTUREGROUP_TERRAIN_HEIGHTMAP`
    - `TextureGroup.TEXTUREGROUP_TERRAIN_WEIGHTMAP`
    - `TextureGroup.TEXTUREGROUP_UI`
    - `TextureGroup.TEXTUREGROUP_VEHICLE`
    - `TextureGroup.TEXTUREGROUP_VEHICLE_NORMAL_MAP`
    - `TextureGroup.TEXTUREGROUP_VEHICLE_SPECULAR`
    - `TextureGroup.TEXTUREGROUP_WEAPON`
    - `TextureGroup.TEXTUREGROUP_WEAPON_NORMAL_MAP`
    - `TextureGroup.TEXTUREGROUP_WEAPON_SPECULAR`
    - `TextureGroup.TEXTUREGROUP_WORLD`
    - `TextureGroup.TEXTUREGROUP_WORLD_NORMAL_MAP`
    - `TextureGroup.TEXTUREGROUP_WORLD_SPECULAR`