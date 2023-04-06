project(
	'stb-wrap',
	'c',
)

incdir = include_directories('.')

stb_c_lexer = static_library(
	'stb_c_lexer',
	[
		'stb_c_lexer.c',
	],
	c_args: [
	],
	include_directories: incdir,
)

stb_c_lexer_dep = declare_dependency(
	link_with: stb_c_lexer,
	include_directories: incdir,
)

stb_divide = static_library(
	'stb_divide',
	[
		'stb_divide.c',
	],
	c_args: [
		# C_INTEGER_DIVISION_TRUNCATES
		# C_INTEGER_DIVISION_FLOORS
	],
	include_directories: incdir,
)

stb_divide_dep = declare_dependency(
	link_with: stb_divide,
	include_directories: incdir,
)

stb_dxt = static_library(
	'stb_dxt',
	[
		'stb_dxt.c',
	],
	c_args: [
	],
	include_directories: incdir,
)

stb_dxt_dep = declare_dependency(
	link_with: stb_dxt,
	include_directories: incdir,
)

stb_easy_font_dep = declare_dependency(
	include_directories: incdir,
)

stb_herringbone_wang_tile = static_library(
	'stb_herringbone_wang_tile',
	[
		'stb_herringbone_wang_tile.c',
	],
	c_args: [
		# STB_HBWANG_RAND()
		# STB_HBWANG_ASSERT(X)
		# STB_HBWANG_STATIC
		# STB_HBWANG_NO_REPITITION_REDUCTION
		# STB_HBWANG_MAX_X
		# STB_HBWANG_MAX_Y
	],
	include_directories: incdir,
)

stb_herringbone_wang_tile_dep = declare_dependency(
	link_with: stb_herringbone_wang_tile,
	include_directories: incdir,
)

stb_hexwave = static_library(
	'stb_hexwave',
	[
		'stb_hexwave.c',
	],
	c_args: [
	],
	include_directories: incdir,
)

stb_hexwave_dep = declare_dependency(
	link_with: stb_hexwave,
	include_directories: incdir,
)

stb_image_resize = static_library(
	'stb_image_resize',
	[
		'stb_image_resize.c',
	],
	c_args: [
		# STBIR_ASSERT(X)
		# STBIR_MALLOC
		# STBIR_FREE
		# STBIR_SATURATE_INT
		# STBIR_DEFAULT_FILTER_UPSAMPLE
		# STBIR_DEFAULT_FILTER_DOWNSAMPLE
		# STBIR_PROGRESS_REPORT
		# STBIR_MAX_CHANNELS
	],
	include_directories: incdir,
)

stb_image_resize_dep = declare_dependency(
	link_with: stb_image_resize,
	include_directories: incdir,
)

stb_image_write = static_library(
	'stb_image_write',
	[
		'stb_image_write.c',
	],
	c_args: [
		# STBIW_ASSERT(X)
		# STBIW_MALLOC
		# STBIW_REALLOC
		# STBIW_FREE
		# STBIW_MEMMOVE
		# STBIW_ZLIB_COMPRESS
		# STBIW_WINDOWS_UTF8
		# STBI_WRITE_NO_STDIO
	],
	include_directories: incdir,
)

stb_image_write_dep = declare_dependency(
	link_with: stb_image_write,
	include_directories: incdir,
)

stb_image = static_library(
	'stb_image',
	[
		'stb_image.c',
	],
	c_args: [
		# STBI_ASSERT(X)
		# STBI_MALLOC
		# STBI_REALLOC
		# STBI_FREE
		# STBI_NO_STDIO
	],
	include_directories: incdir,
)

stb_image_dep = declare_dependency(
	link_with: stb_image,
	include_directories: incdir,
)

stb_include = static_library(
	'stb_include',
	[
		'stb_include.c',
	],
	c_args: [
		# STB_INCLUDE_LINE_GLSL
		# STB_INCLUDE_LINE_NONE
	],
	include_directories: incdir,
)

stb_include_dep = declare_dependency(
	link_with: stb_include,
	include_directories: incdir,
)

stb_perlin = static_library(
	'stb_perlin',
	[
		'stb_perlin.c',
	],
	c_args: [
	],
	include_directories: incdir,
)

stb_perlin_dep = declare_dependency(
	link_with: stb_perlin,
	include_directories: incdir,
)

stb_rect_pack = static_library(
	'stb_rect_pack',
	[
		'stb_rect_pack.c',
	],
	c_args: [
		# STBRP_SORT
		# STBRP_ASSERT
	],
	include_directories: incdir,
)

stb_rect_pack_dep = declare_dependency(
	link_with: stb_rect_pack,
	include_directories: incdir,
)

stb_sprintf = static_library(
	'stb_sprintf',
	[
		'stb_sprintf.c',
	],
	c_args: [
		# STB_SPRINTF_DECORATE
	],
	include_directories: incdir,
)

stb_sprintf_dep = declare_dependency(
	link_with: stb_sprintf,
	include_directories: incdir,
)

stb_truetype = static_library(
	'stb_truetype',
	[
		'stb_truetype.c',
	],
	c_args: [
		# STBTT_RASTERIZER_VERSION
	],
	include_directories: incdir,
)

stb_truetype_dep = declare_dependency(
	link_with: stb_truetype,
	include_directories: incdir,
)

stb_dep = declare_dependency(
	include_directories: [
		'.',
	],
)
