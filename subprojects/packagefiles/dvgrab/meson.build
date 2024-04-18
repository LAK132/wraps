project(
	'dvgrab',
	['c', 'cpp'],
	version: '3.5',
	default_options: [
		'buildtype=release',
		'optimization=3',
	],
)

cxx = meson.get_compiler('cpp')

c_args = []

cpp_args = [
	'-Wno-reorder',
	'-Wno-register',
]

c_cpp_args = [
	'-Wfatal-errors',

	'-D_REENTRANT',
	'-D_FILE_OFFSET_BITS=64',

	'-DPACKAGE="@0@"'.format(meson.project_name()),
	'-DVERSION="@0@"'.format(meson.project_version()),
]

dependencies = [
	dependency('libraw1394', version: '>=1.1.0'),
	dependency('libavc1394', version: '>=0.5.1'),
	dependency('libiec61883', version: '>=1.0.0'),
	dependency('threads'),
]

if cxx.has_header('linux/videodev2.h')
	c_cpp_args += '-DHAVE_LINUX_VIDEODEV2_H=1'
endif

if get_option('with-libdv')
	dependencies += dependency('libdv', version: '>=0.103')
	c_cpp_args += '-DHAVE_LIBDV=1'
endif

if get_option('with-libquicktime')
	dependencies += dependency('libquicktime', 'libquicktimehv', version: '>=0.9.5')
	c_cpp_args += '-DHAVE_LIBQUICKTIME=1'
endif

if get_option('with-libjpeg')
	dependencies += dependency('libjpeg')
	c_cpp_args += '-DHAVE_LIBJPEG=1'
endif

if get_option('with-efence')
	dependencies += dependency('libefence')
	c_cpp_args += '-DHAVE_EFENCE=1'
endif

add_project_arguments(c_cpp_args + cpp_args, language: ['cpp'])
add_project_arguments(c_cpp_args + c_args, language: ['c'])

libdvgrab = static_library(
	'libdvgrab',
	[
		'avi.cc',
		'dvframe.cc',
		'dvgrab.cc',
		'error.cc',
		'filehandler.cc',
		'frame.cc',
		'hdvframe.cc',
		'iec13818-1.cc',
		'iec13818-2.cc',
		'ieee1394io.cc',
		'io.c',
		'raw1394util.c',
		'riff.cc',
		'smiltime.cc',
		'srt.cc',
		'stringutils.cc',
		'v4l2reader.cc',
	],
	dependencies: dependencies,
)

libdvgrab_dep = declare_dependency(
	link_with: libdvgrab,
	dependencies: dependencies,
  include_directories: '.',
)

dvgrab = executable(
	'dvgrab',
	'main.cc',
	dependencies: libdvgrab_dep,
)
