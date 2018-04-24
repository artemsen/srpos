libdir = ${pluginslibdir}
lib_LTLIBRARIES = libsrpos_plugin.la
libsrpos_plugin_la_SOURCES = srpos.c
libsrpos_plugin_la_LDFLAGS = -module -shared -avoid-version -no-undefined -fPIC
libsrpos_plugin_la_CPPFLAGS = -D__PLUGIN__ -DMODULE_STRING=\"srpos\"

EXTRA_DIST = Makefile.mingw vlc_2.2_include
