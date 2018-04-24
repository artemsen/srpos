# Process this file with autoconf to produce a configure script.

AC_PREREQ(2.68)
AC_INIT([libsrpos_plugin], [0.5], [artemsen@gmail.com], [], [http://vlcsrposplugin.sourceforge.net])
AM_INIT_AUTOMAKE([-Wall])
AC_CONFIG_SRCDIR([srpos.c])
AM_PROG_AR
LT_INIT

AC_CANONICAL_HOST
AC_PROG_CC
AC_PROG_CC_C99
AC_C_CONST

AC_ARG_WITH([vlc-include-path],
  [AS_HELP_STRING([--with-vlc-include-path],
    [location of the VLC includes])],
  [CPPFLAGS="$CPPFLAGS -I$withval"],
  [CPPFLAGS="$CPPFLAGS -I./vlc_2.2_include"])

AC_ARG_WITH([vlc-lib-path],
  [AS_HELP_STRING([--with-vlc-lib-path],
    [location of the vlc library (libvlc.so)])],
  [LDFLAGS="$LDFLAGS -L$withval"],
  [])

AC_ARG_WITH([vlc-plugin-path],
  [AS_HELP_STRING([--with-vlc-plugin-path],
    [location of the VLC plugin modules, defaults to /usr/lib/vlc/plugins])],
  [pluginslibdir="$withval"],
  [pluginslibdir="/usr/lib/vlc/plugins"])
AC_SUBST(pluginslibdir)

AC_HEADER_STDC
AC_CHECK_HEADER([vlc_plugin.h], [], [AC_MSG_ERROR(VLC headers not found. Use --with-vlc-include-path option to locate VLC include path.)])
AC_CHECK_LIB([vlc], [main], [], [AC_MSG_ERROR(VLC library not found. Please install libvlc-dev package or use --with-vlc-lib-path option to locate libvlc.so library.)])

AC_CONFIG_FILES([Makefile])
AC_OUTPUT
