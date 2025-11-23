project(
	'lmdb',
	'c',
)

lmdb_dep = subproject('lmdb-wrap').get_variable('lmdb_dep')
meson.override_dependency('lmdb-0.9.31', lmdb_dep)
