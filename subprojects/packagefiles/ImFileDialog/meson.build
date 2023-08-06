project(
	'ImFileDialog-wrap',
	'cpp',
)

includes = include_directories('.')

im_file_dialog = static_library(
	'ImFileDialog',
	[
		'ImFileDialog.cpp',
	],
	override_options: [
		'cpp_std=c++17',
	],
	include_directories: includes,
	dependencies: subproject('imgui-wrap').get_variable('imgui_dep'),
)

im_file_dialog_dep = declare_dependency(
	link_with: im_file_dialog,
	include_directories: includes,
)
