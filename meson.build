# SPDX-License-Identifier: GPL-2.0-only
# SPDX-FileCopyrightText: 2023 Rachel Mant <git@dragonmux.network>
project(
	'libcuefile',
	'c',
	version: '0.0.0',
	meson_version: '>= 0.63',
)

if cxx.get_id() == 'msvc'
	add_project_arguments('-D_CRT_SECURE_NO_WARNINGS', language: 'c')
endif

subdir('include')
subdir('src')

libcuefile_dep = declare_dependency(
	link_with: cuefile,
	include_directories: includes,
	version: meson.project_version()
)
