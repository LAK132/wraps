project(
	'libgphoto2',
	'c',
	meson_version: '>=0.59',
)

libgphoto2_wrap_subprj = subproject('libgphoto2-wrap')
libgphoto2_dep = libgphoto2_wrap_subprj.get_variable('libgphoto2_dep')
libgphoto2_dlls = libgphoto2_wrap_subprj.get_variable('libgphoto2_dlls', [])
libgphoto2_dlls_dep = libgphoto2_wrap_subprj.get_variable('libgphoto2_msys', [])
