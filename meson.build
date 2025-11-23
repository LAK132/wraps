project(
	'imgui',
	'cpp',
	version: 'v1.88',
)

imgui_dep = subproject('imgui-1.88-wrap').get_variable('imgui_dep')
meson.override_dependecy('imgui-1.88', imgui_dep)

imgui_node_editor_dep = subproject('imgui-node-editor-wrap').get_variable('imgui_node_editor_dep')
meson.override_dependecy('imgui-node-editor-0.9.2', imgui_node_editor_dep)

imgui_color_text_edit_dep = subproject('ImGuiColorTextEdit-wrap').get_variable('imgui_color_text_edit_dep')
meson.override_dependecy('imgui_color_text_edit', imgui_color_text_edit_dep)

im_file_dialog_dep = subproject('ImFileDialog-wrap').get_variable('im_file_dialog_dep')
meson.override_dependecy('im_file_dialog', im_file_dialog_dep)
