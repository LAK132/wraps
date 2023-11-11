project(
	'godot-cpp-wrap',
	'cpp',
	meson_version: '>=0.61',
)

cmake = find_program('cmake')

if get_option('buildtype') == 'debug'
	godot_cpp_build_type = 'Debug'
elif get_option('buildtype') == 'release'
	godot_cpp_build_type = 'Release'
elif get_option('buildtype') == 'debugoptimized'
	godot_cpp_build_type = 'RelWithDebInfo'
elif get_option('buildtype') == 'minsize'
	godot_cpp_build_type = 'MinSizeRel'
else
	error('unsupported build type')
endif

godot_cpp_build = custom_target(
	'build-godot-cpp',
	output: ['asdf'],
	console: true,
	command: [
		cmake,
		'-DCMAKE_BUILD_TYPE=' + godot_cpp_build_type,
		'-DCMAKE_INSTALL_PREFIX=@CURRENT_SOURCE_DIR@/build',
		'-S', '@CURRENT_SOURCE_DIR@',
		'-B', '@OUTDIR@',
		'-G', 'Ninja',
	],
)

godot_cpp_build_dir = godot_cpp_build[0].full_path()/'..'

subdir('bin')

godot_cpp = static_library(
	'godot-cpp',
	[
		'empty.cpp',
	],
	link_args: 'bin'/godot_cpp_output,
	link_depends: cmake_generated_godot_cpp_lib,
)

godot_cpp_inc = include_directories(
	'include',
)

godot_cpp_dep = declare_dependency(
	link_whole: godot_cpp,
	include_directories: godot_cpp_inc,
)
