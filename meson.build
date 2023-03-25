# SPDX-License-Identifier: BSD-3-Clause
# SPDX-FileCopyrightText: 2023 Rachel Mant <git@dragonmux.network>
project(
	'libcuefile',
	'c',
	version: '0.0.0',
	meson_version: '>= 0.63',
	default_options: [
		'c_std=gnu99',
	]
)

c = meson.get_compiler('c')
if target_machine.system() == 'windows'
	add_project_arguments('-D_CRT_SECURE_NO_WARNINGS', language: 'c')
endif

add_project_arguments(
	c.get_supported_arguments('-Wno-error=implicit-function-declaration'),
	language: 'c'
)

subdir('include')
subdir('src')

libcuefile_dep = declare_dependency(
	link_with: cuefile,
	include_directories: includes,
	version: meson.project_version()
)
