project(
	'imgui-node-editor-wrap',
	['cpp'],
)

includes = include_directories('.')

imgui_node_editor = static_library(
	'imgui-node-editor',
	[
		'imgui_canvas.cpp',
		'imgui_node_editor.cpp',
		'imgui_node_editor_api.cpp',
		'crude_json.cpp',
	],
	override_options: [
		'cpp_std=c++14',
	],
	include_directories: includes,
	dependencies: subproject('imgui-wrap').get_variable('imgui_dep'),
)

imgui_node_editor_dep = declare_dependency(
	link_with: imgui_node_editor,
	include_directories: includes,
)
