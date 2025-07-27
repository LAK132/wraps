project(
	'libraw-wrap',
	'cpp',
)

cxx = meson.get_compiler('cpp')

if cxx.get_id() == 'msvc'
	c_cpp_args = [
		'-DUNICODE',
		'-DWIN32_LEAN_AND_MEAN',
		'-DNOMINMAX',
		'-EHsc',
		'-MP',
		'-DWIN32',
	]

	cpp_args = []

	c_args = []
else
	c_cpp_args = []

	cpp_args = []

	c_args = []
endif

c_cpp_args += [
	'-D_CRT_SECURE_NO_WARNINGS',
]

if get_option('libraw_static_library')
	c_cpp_args += [ '-DLIBRAW_NODLL' ]
else
	c_cpp_args += [ '-DLIBRAW_BUILDLIB' ]
endif

if get_option('libraw_use_x3ftools')
	c_cpp_args += [ '-DUSE_X3FTOOLS' ]
endif

if get_option('buildtype') != 'debug'
	c_cpp_args += [ '-DNDEBUG' ]
endif

add_project_arguments(c_cpp_args + cpp_args, language: ['cpp'])
add_project_arguments(c_cpp_args + c_args, language: ['c'])

subdir('src')
