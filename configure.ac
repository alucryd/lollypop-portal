AC_PREREQ(2.63)
AC_INIT([lollypop-portal],
        [0.9.0],
        [https://github.com/gnumdk/lollypop-portal],
        [lollypop-portal],
        [https://github.com/gnumdk/lollypop-portal])
AC_CONFIG_MACRO_DIR([m4])
AC_CONFIG_SRCDIR([Makefile.am])
AC_CONFIG_HEADERS(config.h)
AM_INIT_AUTOMAKE([1.11 tar-ustar dist-xz no-dist-gzip -Wno-portability subdir-objects])
AM_MAINTAINER_MODE([enable])
m4_ifdef([AM_SILENT_RULES],[AM_SILENT_RULES([yes])])

AM_PATH_PYTHON(3.0)
AM_PYTHON_CHECK_VERSION(3.0)

PKG_PROG_PKG_CONFIG([0.22])

GLIB_GSETTINGS
GOBJECT_INTROSPECTION_REQUIRE([1.35.9])
PKG_CHECK_MODULES([GTK], [gtk+-3.0 >= 3.14])

GLIB_COMPILE_RESOURCES=`$PKG_CONFIG --variable glib_compile_resources gio-2.0`
AC_SUBST(GLIB_COMPILE_RESOURCES)

AC_CONFIG_FILES([
  Makefile
])
AC_OUTPUT
