AM_CPPFLAGS = \
	-I$(top_srcdir)/include \
	-I$(top_srcdir)

AM_CFLAGS = \
	$(GLOBAL_CFLAGS) \
	$(libusbmuxd_CFLAGS) \
	$(libplist_CFLAGS) \
	$(libgnutls_CFLAGS) \
	$(libtasn1_CFLAGS) \
	$(libgcrypt_CFLAGS) \
	$(openssl_CFLAGS) \
	$(LFS_CFLAGS)

AM_LDFLAGS = \
	$(libusbmuxd_LIBS) \
	$(libplist_LIBS) \
	$(libgnutls_LIBS) \
	$(libtasn1_LIBS) \
	$(libgcrypt_LIBS) \
	$(openssl_LIBS) \
	${libpthread_LIBS}

noinst_LTLIBRARIES = libinternalcommon.la
libinternalcommon_la_LIBADD = 
libinternalcommon_la_LDFLAGS = $(AM_LDFLAGS) -no-undefined
libinternalcommon_la_SOURCES = \
	debug.c debug.h \
	userpref.c userpref.h

if WIN32
libinternalcommon_la_LIBADD += -lole32 -lws2_32
endif
