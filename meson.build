project(
	'libpng',
	'cpp',
	meson_version: '>=0.55',
)

libpng_dep = subproject('libpng-wrap').get_variable('libpng_dep')
meson.override_dependency('libpng-1.6.38', libpng_dep)
