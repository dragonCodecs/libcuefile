# SPDX-License-Identifier: BSD-3-Clause
# SPDX-FileCopyrightText: 2023 Rachel Mant <git@dragonmux.network>
cuefileSrcs = [
	'cd.c',
	'cdtext.c',
	'cue_parse.c',
	'cue_print.c',
	'cue_scan.c',
	'cuefile.c',
	'time.c',
	'toc_parse.c',
	'toc_print.c',
	'toc_scan.c',
]

cuefile = static_library(
	'cuefile',
	cuefileSrcs,
	c_args: ['-DYY_NEVER_INTERACTIVE'],
	include_directories: includes,
	gnu_symbol_visibility: 'inlineshidden',
	install: true
)
