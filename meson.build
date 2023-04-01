project(
	'SDL2',
	'cpp',
)

cmake = import('cmake')

sdl2_opts = cmake.subproject_options()

sdl2_opts.add_cmake_defines({
	'SDL_STATIC': 'ON',
	'SDL_SHARED': 'OFF',
	'SDL_DISABLE_UNINSTALL': 'ON',
	'SDL_DISABLE_INSTALL': 'ON',
})

if get_option('b_vscrt') == 'mt' or get_option('b_vscrt') == 'mtd' or get_option('b_vscrt') == 'static_from_buildtype'
	sdl2_opts.add_cmake_defines({
		'SDL_FORCE_STATIC_VCRT': 'ON',
	})
endif

sdl2_subprj = cmake.subproject('SDL2-wrap', options: sdl2_opts)

sdl2_dep = declare_dependency(
	dependencies: sdl2_subprj.dependency('SDL2_static'),

	# the meson cmake module isn't picking up on the fact that the SDL2_static
	# target is generating headers that later build steps depend on. so here we
	# introduce a custom_target which depends on the SDL2_static lib, and
	# generates a header which is marked as a source file for any later build
	# steps that depen on sdl2_dep
	sources: custom_target(
		'sdl2-dep-delay',
		output: 'sdl2-dep-delay.hpp',
		input: sdl2_subprj.target('SDL2_static'),
		capture: true,
		command: [find_program('python3'), '-c', ''],
	),
)
