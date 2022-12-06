project(
	'llvm',
	'cpp',
	meson_version: '>=0.55',
)

llvm_wrap_subprj = subproject('llvm-wrap')
llvm_dep = llvm_wrap_subprj.get_variable('llvm_dep')
llvm_cmake_generated_headers = llvm_wrap_subprj.get_variable(
	'cmake_generated_headers', [])
