project(
	'libadf',
	'cpp',
	version: '9.0.1'
)

sources = [
	'adf.cpp',
]

headers_adf = [
	'include/adf/adf.h'
]

headers_video = [
	'include/video/adf.h'
]

dependencies = [
	dependency('libdrm'),
]

library(
	'adf',
	sources: sources,
	include_directories: include_directories('include/'),
	dependencies: dependencies,
	version: meson.project_version(),
	soversion: '0',
	install: true
)

pkg = import('pkgconfig')
pkg.generate(
	name: 'libadf',
	libraries: ['-ladf'],
	version: meson.project_version(),
	description: 'libadf',
	subdirs: ['libadf']
)

install_headers(headers_adf, subdir: 'adf')
install_headers(headers_video, subdir: 'video')

