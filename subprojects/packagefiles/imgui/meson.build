project(
	'imgui-wrap',
	'cpp',
)

includes = include_directories('.', 'misc/softraster')

imgui = static_library(
	'imgui',
	[
		'examples/imgui_impl_softraster.cpp',
		'misc/cpp/imgui_stdlib.cpp',
		'imgui_demo.cpp',
		'imgui_draw.cpp',
		'imgui_tables.cpp',
		'imgui_widgets.cpp',
		'imgui.cpp',
	],
	include_directories: includes,
)

imgui_dep = declare_dependency(
	link_with: imgui,
	include_directories: includes,
)
