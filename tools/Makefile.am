AM_CPPFLAGS =						\
	$(GLIB_CFLAGS)					\
	$(GUDEV_CFLAGS)					\
	$(USB_CFLAGS)					\
	-DBINDIR=\"$(bindir)\"			 	\
	-DDATADIR=\"$(datadir)\"			\
	-DPREFIX=\""$(prefix)"\" 			\
	-DSYSCONFDIR=\""$(sysconfdir)"\" 		\
	-DLIBDIR=\""$(libdir)"\" 			\
	-DVERSION="\"$(VERSION)\"" 			\
	-DG_LOG_DOMAIN=\"GUsb\"				\
	-DG_USB_API_IS_SUBJECT_TO_CHANGE		\
	-I$(top_srcdir)					\
	-I$(top_builddir)

GUSB_LIBS =						\
	$(top_builddir)/gusb/libgusb.la

noinst_PROGRAMS =					\
	gusb

gusb_SOURCES =						\
	gusb-main.c

gusb_LDADD =						\
	$(USB_LIBS)					\
	$(GLIB_LIBS)					\
	$(GUDEV_LIBS)					\
	$(GUSB_LIBS)

gusb_CFLAGS =						\
	$(WARNINGFLAGS_C)

clean-local:
	rm -f *~

CLEANFILES = $(BUILT_SOURCES)

DISTCLEANFILES =

MAINTAINERCLEANFILES =					\
	*~			      			\
	Makefile.in

-include $(top_srcdir)/git.mk
