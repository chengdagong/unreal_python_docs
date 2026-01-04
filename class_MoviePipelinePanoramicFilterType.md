# unreal.MoviePipelinePanoramicFilterType

```python
class unreal.MoviePipelinePanoramicFilterType
```


**Bases:** ``EnumBase``


EMovie Pipeline Panoramic Filter Type

**C++ Source:**

- **Plugin**: MovieRenderPipeline

- **Module**: MovieRenderPipelineCore

- **File**: MoviePipelinePanoramicBlenderBase.h


BILINEAR _: MoviePipelinePanoramicFilterType_ _=Ellipsis_

2x2 Bilinear Interpolation. Fastest, nearly the same quality as other options.

**Type:**

0

CATMULL _: MoviePipelinePanoramicFilterType_ _=Ellipsis_

Cubic Catmull-Rom interpolation. Slightly sharper than other results. Uses B=0, C=1/2 in parameterized cubic equation.

**Type:**

1

MITCHELL _: MoviePipelinePanoramicFilterType_ _=Ellipsis_

Cubic Mitchell-Netravali interpolation. More neutral look. Uses B=0.33, C=0.33 in parameterized cubic equation.

**Type:**

2

### Table of Contents

- `unreal.MoviePipelinePanoramicFilterType`
  - `MoviePipelinePanoramicFilterType`
    - `MoviePipelinePanoramicFilterType.BILINEAR`
    - `MoviePipelinePanoramicFilterType.CATMULL`
    - `MoviePipelinePanoramicFilterType.MITCHELL`