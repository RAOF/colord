AM_CPPFLAGS =						\
	$(PIE_CFLAGS)					\
	$(GLIB_CFLAGS)					\
	$(GTK_CFLAGS)					\
	-I$(top_srcdir)					\
	-I$(top_srcdir)/lib				\
	-I$(top_builddir)/lib				\
	-I$(top_srcdir)/lib/colord			\
	-DG_LOG_DOMAIN=\"Cd\"				\
	-DCD_COMPILATION				\
	-DCD_DISABLE_DEPRECATED				\
	-DLIBEXECDIR=\"$(libexecdir)\"			\
	-DDATADIR=\"$(datadir)\"			\
	-DSYSCONFDIR=\""$(sysconfdir)"\"		\
	-DVERSION="\"$(VERSION)\""			\
	-DLOCALEDIR=\""$(localedir)"\"

COLORD_LIBS =						\
	$(top_builddir)/lib/colord/libcolordprivate.la	\
	$(top_builddir)/lib/colord/libcolord.la

bin_PROGRAMS =						\
	cd-create-profile				\
	cd-iccdump					\
	cd-it8						\
	cd-fix-profile

if HAVE_DAEMON
bin_PROGRAMS +=						\
	colormgr
endif

colormgr_SOURCES =					\
	cd-util.c

colormgr_LDADD =					\
	$(COLORD_LIBS)					\
	$(GLIB_LIBS)

colormgr_LDFLAGS =					\
	$(PIE_LDFLAGS)

colormgr_CFLAGS =					\
	$(WARNINGFLAGS_C)

cd_fix_profile_SOURCES =				\
	cd-fix-profile.c

cd_fix_profile_LDADD =					\
	$(GLIB_LIBS)					\
	$(LCMS_LIBS)					\
	$(COLORD_LIBS)					\
	-lm

cd_fix_profile_CFLAGS =					\
	$(WARNINGFLAGS_C)

cd_fix_profile_LDFLAGS =				\
	$(PIE_LDFLAGS)

cd_iccdump_SOURCES =					\
	cd-iccdump.c

cd_iccdump_LDADD =					\
	$(GLIB_LIBS)					\
	$(LCMS_LIBS)					\
	$(COLORD_LIBS)					\
	-lm

cd_iccdump_LDFLAGS =					\
	$(PIE_LDFLAGS)

cd_iccdump_CFLAGS =					\
	$(WARNINGFLAGS_C)

cd_it8_SOURCES =					\
	cd-it8.c

cd_it8_LDADD =						\
	$(GLIB_LIBS)					\
	$(LCMS_LIBS)					\
	$(COLORD_LIBS)					\
	-lm

cd_it8_LDFLAGS =					\
	$(PIE_LDFLAGS)

cd_it8_CFLAGS =						\
	$(WARNINGFLAGS_C)

cd_create_profile_SOURCES =				\
	cd-create-profile.c

cd_create_profile_LDADD =				\
	$(GLIB_LIBS)					\
	$(LCMS_LIBS)					\
	$(COLORD_LIBS)					\
	-lm

cd_create_profile_LDFLAGS =				\
	$(PIE_LDFLAGS)

cd_create_profile_CFLAGS =				\
	$(WARNINGFLAGS_C)

MAINTAINERCLEANFILES = *.a

-include $(top_srcdir)/git.mk
