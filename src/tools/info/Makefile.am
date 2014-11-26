#
# Copyright (C) Mellanox Technologies Ltd. 2001-2014.  ALL RIGHTS RESERVED.
#
# $COPYRIGHT$
# $HEADER$
#

bin_PROGRAMS          = ucx_info
AM_CPPFLAGS           = \
    -I$(abs_top_srcdir)/src \
    -I$(abs_top_builddir)/src

BUILT_SOURCES = build_config.h
DISTCLEANFILES = build_config.h

#
# Produce a C header file which contains all defined variables from config.h
#
build_config.h: $(top_builddir)/config.h Makefile
	$(SED) -nr 's:\s*#define\s+(\w+)(\s+(\w+)|\s+(".*")|\s*)$$:{"\1", UCS_PP_MAKE_STRING(\3\4)},:p' <$(top_builddir)/config.h >$@


ucx_info_SOURCES  = ucx_info.c
ucx_info_LDADD    = \
     $(abs_top_builddir)/src/uct/libuct.la \
     $(abs_top_builddir)/src/ucs/libucs.la

noinst_HEADERS = \
	build_config.h