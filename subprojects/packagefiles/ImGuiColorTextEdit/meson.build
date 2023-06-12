project(
	'ImGuiColorTextEdit-wrap',
	'cpp',
)

includes = include_directories('.')

imgui_color_text_edit = static_library(
	'ImGuiColorTextEdit',
	[
		'TextEditor.cpp',
	],
	override_options: [
		'cpp_std=c++11',
	],
	include_directories: includes,
	dependencies: subproject('imgui-wrap').get_variable('imgui_dep'),
)

imgui_color_text_edit_dep = declare_dependency(
	link_with: imgui_color_text_edit,
	include_directories: includes,
)
