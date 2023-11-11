godot_cpp_build_dep = custom_target(
	'godot-cpp-dep',
	output: 'node.hpp',
	depends: cmake_generated_godot_cpp_lib,
	capture: true,
	command: [
		import('python').find_installation(),
		'-c', 'open(\'@OUTPUT0@\', \'w\').close()',
	],
)
