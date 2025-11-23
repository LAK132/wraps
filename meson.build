project(
	'lua',
	'c',
)

lua_subprj = subproject('lua-wrap')

lua_core_dep = lua_subprj.get_variable('lua_core_dep')
meson.override_dependency('lua-5.4.4-core', lua_core_dep)

lua_lib_dep = lua_subprj.get_variable('lua_lib_dep')
meson.override_dependency('lua-5.4.4', lua_lib_dep)

lua = lua_subprj.get_variable('lua')
meson.override_find_program('lua-5.4.4', lua)

luac = lua_subprj.get_variable('luac')
meson.override_find_program('luac-5.4.4', luac)
