#
# Copyright (C) Mellanox Technologies Ltd. 2001-2014.  ALL RIGHTS RESERVED.
# See file LICENSE for terms.
#

lib_LTLIBRARIES     = libucp.la

libucp_la_CFLAGS   =
libucp_la_LIBS     =
libucp_la_CPPFLAGS = -I$(abs_top_srcdir)/src -I$(abs_top_builddir)/src
libucp_la_LDFLAGS  = -ldl -version-info $(SOVERSION)
libucp_la_LIBADD   = ../ucs/libucs.la ../uct/libuct.la
libucp_ladir       = $(includedir)/ucp

nobase_dist_libucp_la_HEADERS = \
	api/ucp_def.h \
	api/ucp_version.h \
	api/ucp.h

noinst_HEADERS = \
	core/ucp_context.h \
	core/ucp_ep.h \
	core/ucp_ep.inl \
	core/ucp_mm.h \
	core/ucp_request.h \
	core/ucp_request.inl \
	core/ucp_worker.h \
	dt/dt_contig.h \
	dt/dt_generic.h \
	proto/proto.h \
	proto/proto_am.inl \
	tag/eager.h \
	tag/match.h \
	tag/rndv.h \
	wireup/address.h \
	wireup/stub_ep.h \
	wireup/wireup.h

libucp_la_SOURCES = \
	amo/basic_amo.c \
	core/ucp_context.c \
	core/ucp_ep.c \
	core/ucp_mm.c \
	core/ucp_request.c \
	core/ucp_rkey.c \
	core/ucp_version.c \
	core/ucp_worker.c \
	dt/dt_contig.c \
	dt/dt_generic.c \
	proto/proto_am.c \
	rma/basic_rma.c \
	tag/eager_rcv.c \
	tag/eager_snd.c \
	tag/probe.c \
	tag/rndv.c \
	tag/tag_recv.c \
	tag/tag_send.c \
	wireup/address.c \
	wireup/select.c \
	wireup/stub_ep.c \
	wireup/wireup.c
