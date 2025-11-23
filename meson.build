project(
	'llvm',
	'cpp',
	meson_version: '>=0.55',
)

if get_option('llvm_from_source')
	llvm_dep = subproject('llvm-wrap').get_variable('llvm_dep')
	meson.override_dependency('llvm-15.0.1', llvm_dep)
else
	llvm_components = []

	foreach target : get_option('llvm_components')
		llvm_components += target.to_lower()
	endforeach

	foreach target : get_option('llvm_install_components')
		llvm_components += target.to_lower()
	endforeach

	llvm_dep = dependency(
		'llvm',
		version: '>= 15',
		modules: llvm_components,
		static: false,
		disabler: true,
		required: false,
	)
endif
