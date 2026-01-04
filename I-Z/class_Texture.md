# unreal.Texture

```python
class unreal.Texture(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``StreamableRenderAsset``


**C++ Source:**

- **Module**: Engine

- **File**: Texture.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `adjust_brightness` (float): [Read-Write] Static texture brightness adjustment (scales HSV value.) (Non-destructive; Requires texture source art to be available.)

- `adjust_brightness_curve` (float): [Read-Write] Static texture curve adjustment (raises HSV value to the specified power.) (Non-destructive; Requires texture source art to be available.)

- `adjust_hue` (float): [Read-Write] Static texture hue adjustment (0 - 360) (offsets HSV hue by value in degrees.) (Non-destructive; Requires texture source art to be available.)

- `adjust_max_alpha` (float): [Read-Write] Remaps the alpha to the specified min/max range, defines the new value of 1 (Non-destructive; Requires texture source art to be available.)

- `adjust_min_alpha` (float): [Read-Write] Remaps the alpha to the specified min/max range, defines the new value of 0 (Non-destructive; Requires texture source art to be available.)

- `adjust_rgb_curve` (float): [Read-Write] Static texture RGB curve adjustment (raises linear-space RGB color to the specified power.) (Non-destructive; Requires texture source art to be available.)

- `adjust_saturation` (float): [Read-Write] Static texture saturation adjustment (scales HSV saturation.) (Non-destructive; Requires texture source art to be available.)

- `adjust_vibrance` (float): [Read-Write] Static texture “vibrance” adjustment (0 - 1) (HSV saturation algorithm adjustment.) (Non-destructive; Requires texture source art to be available.)

- `alpha_coverage_thresholds` (Vector4): [Read-Write] Alpha values per channel to compare to when preserving alpha coverage. 0 means disable channel. Typical good values in 0.5 - 0.9, not 1.0

- `asset_import_data` (AssetImportData): [Read-Only]

- `asset_user_data` (Array[AssetUserData]): [Read-Write] Array of user data stored with the asset

- `availability` (TextureAvailability): [Read-Write] Whether the texture will be encoded to a gpu format and uploaded to the graphics card, or kept on the CPU for access by gamecode / blueprint.
For CPU availability, the texture will still upload a tiny black texture as a placeholder. Only applies to 2d textures.

- `chroma_key_color` (Color): [Read-Write] The color that will be replaced with transparent black if chroma keying is enabled

- `chroma_key_texture` (bool): [Read-Write] Whether to chroma key the image, replacing any pixels that match ChromaKeyColor with transparent black

- `chroma_key_threshold` (float): [Read-Write] The threshold that components have to match for the texel to be considered equal to the ChromaKeyColor when chroma keying (<=, set to 0 to require a perfect exact match)

- `composite_power` (float): [Read-Write] default 1, high values result in a stronger effect e.g 1, 2, 4, 8
this is not a slider because the texture update would not be fast enough

- `composite_texture` (Texture): [Read-Write]

- `composite_texture_mode` (CompositeTextureMode): [Read-Write] defines how the CompositeTexture is applied, e.g. CTM\_RoughnessFromNormalAlpha

- `compress_final` (bool): [Read-Write] If enabled, compress with Final quality during this Editor session.

- `compression_cache_id` (Guid): [Read-Write] Change this optional ID to force the texture to be recompressed by changing its cache key.

- `compression_no_alpha` (bool): [Read-Write] If enabled, the texture’s alpha channel will be forced to opaque for any compressed texture output format. Does not apply if output format is uncompressed RGBA.

- `compression_quality` (TextureCompressionQuality): [Read-Write] The compression quality for generated ASTC textures (i.e. mobile platform textures).

- `compression_settings` (TextureCompressionSettings): [Read-Write] Compression settings to use when building the texture.

- `cook_platform_tiling_settings` (TextureCookPlatformTilingSettings): [Read-Write] If the platform supports it, tile the texture when cooking, or keep it linear and tile it when it’s actually submitted to the GPU.

- `defer_compression` (bool): [Read-Write] If enabled, defer compression of the texture until save or manually compressed in the texture editor.

- `do_scale_mips_for_alpha_coverage` (bool): [Read-Write] Whether mip RGBA should be scaled to preserve the number of pixels with Value >= AlphaCoverageThresholds. AlphaCoverageThresholds are ignored if this is off.

- `downscale` (PerPlatformFloat): [Read-Write] Downscale source texture, applied only to 2d textures without mips
< 1.0 - use scale value from texture group
1.0 - do not scale texture
\> 1.0 - scale texure

- `downscale_options` (TextureDownscaleOptions): [Read-Write] Texture downscaling options

- `filter` (TextureFilter): [Read-Write] The texture filtering mode to use when sampling this texture.

- `flip_green_channel` (bool): [Read-Write] When true the texture’s green channel will be inverted. This is useful for some normal maps.

- `global_force_mip_levels_to_be_resident` (bool): [Read-Write] Global and serialized version of ForceMiplevelsToBeResident.

- `lod_bias` (int32): [Read-Write] A bias to the index of the top mip level to use. That is, number of mip levels to drop when cooking.

- `lod_group` (TextureGroup): [Read-Write] Texture group this texture belongs to

- `lossy_compression_amount` (TextureLossyCompressionAmount): [Read-Write] How aggressively should any relevant lossy compression be applied. For compressors that support EncodeSpeed (i.e. Oodle), this is only

applied if enabled (see Project Settings -> Texture Encoding). Note that this is _in addition_ to any
unavoidable loss due to the target format - selecting “No Lossy Compression” will not result in zero distortion for BCn formats.

- `max_texture_size` (int32): [Read-Write] The maximum resolution for generated textures. A value of 0 means the maximum size for the format on each platform.

- `mip_gen_settings` (TextureMipGenSettings): [Read-Write] Per asset specific setting to define the mip-map generation properties like sharpening and kernel size.

- `mip_load_options` (TextureMipLoadOptions): [Read-Write] The texture mip load options.

- `never_stream` (bool): [Read-Write]

- `normalize_normals` (bool): [Read-Write] Normalize colors in Normal Maps after mip generation for better and sharper quality; recommended on if not required to match legacy behavior.

- `num_cinematic_mip_levels` (int32): [Read-Write] Number of mip-levels to use for cinematic quality.

- `oodle_preserve_extremes` (bool): [Read-Write] If set to true, then Oodle encoder preserves 0 and 255 (0.0 and 1.0) values exactly in alpha channel for BC3/BC7 and in all channels for BC4/BC5.

- `oodle_texture_sdk_version` (Name): [Read-Write] Oodle Texture SDK Version to encode with. Enter ‘latest’ to update; ‘None’ preserves legacy encoding to avoid patches.

- `pad_with_border_color` (bool): [Read-Write] If set to true, texture padding will be performed using colors of the border pixels. This can be used to improve quality of the generated mipmaps for padded textures.

- `padding_color` (Color): [Read-Write] The color used to pad the texture out if it is padded due to PowerOfTwoMode

- `power_of_two_mode` (TexturePowerOfTwoSetting): [Read-Write] How to pad the texture to a power of 2 size (if necessary)

- `preserve_border` (bool): [Read-Write] When true the texture’s border will be preserved during mipmap generation.

- `resize_during_build_x` (int32): [Read-Write] Width of the resized texture when using “Resize To Specific Resolution” padding and resizing option. If set to zero, original width will be used.

- `resize_during_build_y` (int32): [Read-Write] Width of the resized texture when using “Resize To Specific Resolution” padding and resizing option. If set to zero, original height will be used.

- `source_color_settings` (TextureSourceColorSettings): [Read-Write] Texture color management settings: source encoding and color space.

- `srgb` (bool): [Read-Write] Whether Texture and its source are in SRGB Gamma color space. Can only be used with 8-bit and compressed formats. This should be unchecked if using alpha channels individually as masks.

- `use_legacy_gamma` (bool): [Read-Write] A flag for using the simplified legacy gamma space e.g pow(color,1/2.2) for converting from FColor to FLinearColor, if we’re doing sRGB.

- `use_new_mip_filter` (bool): [Read-Write] Disable for legacy compatibility. New and changed textures should set this to use modern improved image processing.

- `use_virtual_texture_streaming_priority` (bool): [Read-Write] Override the virtual texture streaming priority set on this texture by the texture LOD group.

- `virtual_texture_prefetch_mips` (uint8): [Read-Write] The number of mips that a virtual texture can stream using the traditional CPU texture streaming system.
In most cases this should be 0 because the virtual texture GPU feedback is sufficient and will minimize memory usage.
But CPU prefetching can be used in some cases to avoid late appearance of mips.

- `virtual_texture_streaming` (bool): [Read-Write] Is this texture streamed in using VT

- `virtual_texture_streaming_priority` (VTProducerPriority): [Read-Write] Priority to use when using virtual texture streaming for this texture.



---

**add_asset_user_data_of_class**( _user_data_class_) → `bool`

Creates and adds an instance of the provided AssetUserData class to the target asset.

Parameters:

**user\_data\_class** ( _type_ _(_ _Class_ _)_) – UAssetUserData sub class to create

Returns:

Whether or not an instance of InUserDataClass was succesfully added

Return type:

bool


---

_property_ `adjust_brightness`: float

[Read-Write] Static texture brightness adjustment (scales HSV value.) (Non-destructive; Requires texture source art to be available.)

**Type:**

( float)


---

_property_ `adjust_brightness_curve`: float

[Read-Write] Static texture curve adjustment (raises HSV value to the specified power.) (Non-destructive; Requires texture source art to be available.)

**Type:**

( float)


---

_property_ `adjust_hue`: float

[Read-Write] Static texture hue adjustment (0 - 360) (offsets HSV hue by value in degrees.) (Non-destructive; Requires texture source art to be available.)

**Type:**

( float)


---

_property_ `adjust_max_alpha`: float

[Read-Write] Remaps the alpha to the specified min/max range, defines the new value of 1 (Non-destructive; Requires texture source art to be available.)

**Type:**

( float)


---

_property_ `adjust_min_alpha`: float

[Read-Write] Remaps the alpha to the specified min/max range, defines the new value of 0 (Non-destructive; Requires texture source art to be available.)

**Type:**

( float)


---

_property_ `adjust_rgb_curve`: float

[Read-Write] Static texture RGB curve adjustment (raises linear-space RGB color to the specified power.) (Non-destructive; Requires texture source art to be available.)

**Type:**

( float)


---

_property_ `adjust_saturation`: float

[Read-Write] Static texture saturation adjustment (scales HSV saturation.) (Non-destructive; Requires texture source art to be available.)

**Type:**

( float)


---

_property_ `adjust_vibrance`: float

[Read-Write] Static texture “vibrance” adjustment (0 - 1) (HSV saturation algorithm adjustment.) (Non-destructive; Requires texture source art to be available.)

**Type:**

( float)


---

_property_ `alpha_coverage_thresholds`: Vector4

[Read-Write] Alpha values per channel to compare to when preserving alpha coverage. 0 means disable channel. Typical good values in 0.5 - 0.9, not 1.0

**Type:**

( Vector4)


---

_property_ `availability`: TextureAvailability

[Read-Write] Whether the texture will be encoded to a gpu format and uploaded to the graphics card, or kept on the CPU for access by gamecode / blueprint.
For CPU availability, the texture will still upload a tiny black texture as a placeholder. Only applies to 2d textures.

**Type:**

( TextureAvailability)


---

**blueprint_get_built_texture_size**() → `Vector3fGet the dimensions of the largest mip of the texture when built, accounting for LODBias and other constraints`

Returns the 3d size when built for the current platform. Does not cause texture to get built.

Return type:

Vector3f


---

**blueprint_get_memory_size**() → `int64`

Gets the memory size of the texture, in bytes.
This is the size in GPU memory of the built platformdata, accounting for LODBias, etc.
Returns zero for error.

Return type:

int64

blueprint\_get\_texture\_source\_disk\_and\_memory\_size( _)->(out\_disk\_size=int64_, _out\_memory\_size=int64_)

Gets the memory size of the texture source top mip, in bytes, and the size on disk of the asset, which may be compressed.
Uses texture source, not available in runtime games.
Does not cause texture source to be loaded, queries cached values.
Returns zero for error.

Returns:

out\_disk\_size (int64):

out\_memory\_size (int64):

Return type:

tuple


---

**blueprint_get_texture_source_id_string**() → `strorNone`

Return the ID for the texture source.
If the source isn’t valid or editor data isn’t available, returns false.

Returns:

out\_texture\_source\_id (str):

Return type:

str or None


---

_property_ `chroma_key_color`: Color

[Read-Write] The color that will be replaced with transparent black if chroma keying is enabled

**Type:**

( Color)


---

_property_ `chroma_key_texture`: bool

[Read-Write] Whether to chroma key the image, replacing any pixels that match ChromaKeyColor with transparent black

**Type:**

( bool)


---

_property_ `chroma_key_threshold`: float

[Read-Write] The threshold that components have to match for the texel to be considered equal to the ChromaKeyColor when chroma keying (<=, set to 0 to require a perfect exact match)

**Type:**

( float)


---

_property_ `composite_power`: float

[Read-Write] default 1, high values result in a stronger effect e.g 1, 2, 4, 8
this is not a slider because the texture update would not be fast enough

**Type:**

( float)


---

_property_ `composite_texture`: Texture

[Read-Write]

**Type:**

( Texture)


---

_property_ `composite_texture_mode`: CompositeTextureMode

[Read-Write] defines how the CompositeTexture is applied, e.g. CTM\_RoughnessFromNormalAlpha

**Type:**

( CompositeTextureMode)


---

_property_ `compress_final`: bool

[Read-Write] If enabled, compress with Final quality during this Editor session.

**Type:**

( bool)


---

_property_ `compression_no_alpha`: bool

[Read-Write] If enabled, the texture’s alpha channel will be forced to opaque for any compressed texture output format. Does not apply if output format is uncompressed RGBA.

**Type:**

( bool)


---

_property_ `compression_quality`: TextureCompressionQuality

[Read-Write] The compression quality for generated ASTC textures (i.e. mobile platform textures).

**Type:**

( TextureCompressionQuality)


---

_property_ `compression_settings`: TextureCompressionSettings

[Read-Write] Compression settings to use when building the texture.

**Type:**

( TextureCompressionSettings)


---

**compute_texture_source_channel_min_max**() → `(out_color_min=LinearColor,out_color_max=LinearColor)orNone`

Scan the texture source pixels to compute the min & max values of the RGBA channels.
Uses texture source, not available in runtime games.
Causes texture source data to be loaded, is computed by scanning pixels when called.
Will set Min=Max=zero and return false on failure

Returns:

out\_color\_min (LinearColor):

out\_color\_max (LinearColor):

Return type:

tuple or None


---

_property_ `cook_platform_tiling_settings`: TextureCookPlatformTilingSettings

[Read-Write] If the platform supports it, tile the texture when cooking, or keep it linear and tile it when it’s actually submitted to the GPU.

**Type:**

( TextureCookPlatformTilingSettings)


---

_property_ `defer_compression`: bool

[Read-Write] If enabled, defer compression of the texture until save or manually compressed in the texture editor.

**Type:**

( bool)


---

_property_ `do_scale_mips_for_alpha_coverage`: bool

[Read-Write] Whether mip RGBA should be scaled to preserve the number of pixels with Value >= AlphaCoverageThresholds. AlphaCoverageThresholds are ignored if this is off.

**Type:**

( bool)


---

**export_to_disk**( _filename_, _options_) → `None`

Export the specified texture to disk

Parameters:

- **filename** ( _str_) – The filename on disk to save as

- **options** ( _ImageWriteOptions_) – Parameters defining the various export options



---

_property_ `filter`: TextureFilter

[Read-Write] The texture filtering mode to use when sampling this texture.

**Type:**

( TextureFilter)


---

_property_ `flip_green_channel`: bool

[Read-Write] When true the texture’s green channel will be inverted. This is useful for some normal maps.

**Type:**

( bool)


---

**get_asset_user_data_of_class**( _user_data_class_) → `AssetUserData`

Returns an instance of the provided AssetUserData class if it’s contained in the target asset.

Parameters:

**user\_data\_class** ( _type_ _(_ _Class_ _)_) – UAssetUserData sub class to get

Returns:

The instance of the UAssetUserData class contained, or null if it doesn’t exist

Return type:

AssetUserData


---

**get_texture_streaming_method**() → `TextureStreamingMethod`

Returns the type of streaming the texture is currently using on the current platform. (None/Streamed/Virtual) \*

Return type:

TextureStreamingMethod


---

**has_asset_user_data_of_class**( _user_data_class_) → `bool`

Checks whether or not an instance of the provided AssetUserData class is contained.

Parameters:

**user\_data\_class** ( _type_ _(_ _Class_ _)_) – UAssetUserData sub class to check for

Returns:

Whether or not an instance of InUserDataClass was found

Return type:

bool


---

_property_ `lod_bias`: int

[Read-Write] A bias to the index of the top mip level to use. That is, number of mip levels to drop when cooking.

**Type:**

(int32)


---

_property_ `lod_group`: TextureGroup

[Read-Write] Texture group this texture belongs to

**Type:**

( TextureGroup)


---

_property_ `lossy_compression_amount`: TextureLossyCompressionAmount

[Read-Write] How aggressively should any relevant lossy compression be applied. For compressors that support EncodeSpeed (i.e. Oodle), this is only
applied if enabled (see Project Settings -> Texture Encoding). Note that this is _in addition_ to any
unavoidable loss due to the target format - selecting “No Lossy Compression” will not result in zero distortion for BCn formats.

**Type:**

( TextureLossyCompressionAmount)


---

_property_ `max_texture_size`: int

[Read-Write] The maximum resolution for generated textures. A value of 0 means the maximum size for the format on each platform.

**Type:**

(int32)


---

_property_ `mip_gen_settings`: TextureMipGenSettings

[Read-Write] Per asset specific setting to define the mip-map generation properties like sharpening and kernel size.

**Type:**

( TextureMipGenSettings)


---

_property_ `mip_load_options`: TextureMipLoadOptions

[Read-Write] The texture mip load options.

**Type:**

( TextureMipLoadOptions)


---

_property_ `normalize_normals`: bool

[Read-Write] Normalize colors in Normal Maps after mip generation for better and sharper quality; recommended on if not required to match legacy behavior.

**Type:**

( bool)


---

_property_ `oodle_preserve_extremes`: bool

[Read-Write] If set to true, then Oodle encoder preserves 0 and 255 (0.0 and 1.0) values exactly in alpha channel for BC3/BC7 and in all channels for BC4/BC5.

**Type:**

( bool)


---

_property_ `oodle_texture_sdk_version`: Name

[Read-Write] Oodle Texture SDK Version to encode with. Enter ‘latest’ to update; ‘None’ preserves legacy encoding to avoid patches.

**Type:**

( Name)


---

_property_ `pad_with_border_color`: bool

[Read-Write] If set to true, texture padding will be performed using colors of the border pixels. This can be used to improve quality of the generated mipmaps for padded textures.

**Type:**

( bool)


---

_property_ `padding_color`: Color

[Read-Write] The color used to pad the texture out if it is padded due to PowerOfTwoMode

**Type:**

( Color)


---

_property_ `power_of_two_mode`: TexturePowerOfTwoSetting

[Read-Write] How to pad the texture to a power of 2 size (if necessary)

**Type:**

( TexturePowerOfTwoSetting)


---

_property_ `preserve_border`: bool

[Read-Write] When true the texture’s border will be preserved during mipmap generation.

**Type:**

( bool)


---

_property_ `resize_during_build_x`: int

[Read-Write] Width of the resized texture when using “Resize To Specific Resolution” padding and resizing option. If set to zero, original width will be used.

**Type:**

(int32)


---

_property_ `resize_during_build_y`: int

[Read-Write] Width of the resized texture when using “Resize To Specific Resolution” padding and resizing option. If set to zero, original height will be used.

**Type:**

(int32)


---

**set_virtual_texture_streaming**( _virtual_texture_streaming_) → `None`

Set Virtual Texture Streaming

Parameters:

**virtual\_texture\_streaming** ( _bool_)


---

_property_ `source_color_settings`: TextureSourceColorSettings

source encoding and color space.

**Type:**

( TextureSourceColorSettings)

**Type:**

[Read-Write] Texture color management settings


---

_property_ `srgb`: bool

[Read-Write] Whether Texture and its source are in SRGB Gamma color space. Can only be used with 8-bit and compressed formats. This should be unchecked if using alpha channels individually as masks.

**Type:**

( bool)


---

_property_ `use_legacy_gamma`: bool

[Read-Write] A flag for using the simplified legacy gamma space e.g pow(color,1/2.2) for converting from FColor to FLinearColor, if we’re doing sRGB.

**Type:**

( bool)


---

_property_ `use_new_mip_filter`: bool

[Read-Write] Disable for legacy compatibility. New and changed textures should set this to use modern improved image processing.

**Type:**

( bool)


---

_property_ `virtual_texture_streaming`: bool

[Read-Only] Is this texture streamed in using VT

**Type:**

( bool)


---

_property_ `virtual_texture_streaming_priority`: VTProducerPriority

[Read-Write] Priority to use when using virtual texture streaming for this texture.

**Type:**

( VTProducerPriority)

### Table of Contents

- `unreal.Texture`
  - `Texture`
    - `Texture.add_asset_user_data_of_class()`
    - `Texture.adjust_brightness`
    - `Texture.adjust_brightness_curve`
    - `Texture.adjust_hue`
    - `Texture.adjust_max_alpha`
    - `Texture.adjust_min_alpha`
    - `Texture.adjust_rgb_curve`
    - `Texture.adjust_saturation`
    - `Texture.adjust_vibrance`
    - `Texture.alpha_coverage_thresholds`
    - `Texture.availability`
    - `Texture.blueprint_get_built_texture_size()`
    - `Texture.blueprint_get_memory_size()`
    - `Texture.blueprint_get_texture_source_disk_and_memory_size()`
    - `Texture.blueprint_get_texture_source_id_string()`
    - `Texture.chroma_key_color`
    - `Texture.chroma_key_texture`
    - `Texture.chroma_key_threshold`
    - `Texture.composite_power`
    - `Texture.composite_texture`
    - `Texture.composite_texture_mode`
    - `Texture.compress_final`
    - `Texture.compression_no_alpha`
    - `Texture.compression_quality`
    - `Texture.compression_settings`
    - `Texture.compute_texture_source_channel_min_max()`
    - `Texture.cook_platform_tiling_settings`
    - `Texture.defer_compression`
    - `Texture.do_scale_mips_for_alpha_coverage`
    - `Texture.export_to_disk()`
    - `Texture.filter`
    - `Texture.flip_green_channel`
    - `Texture.get_asset_user_data_of_class()`
    - `Texture.get_texture_streaming_method()`
    - `Texture.has_asset_user_data_of_class()`
    - `Texture.lod_bias`
    - `Texture.lod_group`
    - `Texture.lossy_compression_amount`
    - `Texture.max_texture_size`
    - `Texture.mip_gen_settings`
    - `Texture.mip_load_options`
    - `Texture.normalize_normals`
    - `Texture.oodle_preserve_extremes`
    - `Texture.oodle_texture_sdk_version`
    - `Texture.pad_with_border_color`
    - `Texture.padding_color`
    - `Texture.power_of_two_mode`
    - `Texture.preserve_border`
    - `Texture.resize_during_build_x`
    - `Texture.resize_during_build_y`
    - `Texture.set_virtual_texture_streaming()`
    - `Texture.source_color_settings`
    - `Texture.srgb`
    - `Texture.use_legacy_gamma`
    - `Texture.use_new_mip_filter`
    - `Texture.virtual_texture_streaming`
    - `Texture.virtual_texture_streaming_priority`