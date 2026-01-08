AC_PREREQ(2.57)
AC_INIT([xlibre-xf86-input-egalax],
        25.0.0,
        [https://github.com/X11Libre/xf86-input-egalax/issues]
        xlibre-xf86-input-egalax)

AC_CONFIG_SRCDIR([Makefile.am])
AC_CONFIG_AUX_DIR(.)
AM_INIT_AUTOMAKE([dist-bzip2])

m4_ifndef([XORG_MACROS_VERSION], [AC_FATAL([must install xorg-macros 1.2 or late
r before running autoconf/autogen])])
XORG_MACROS_VERSION(1.2)
AM_CONFIG_HEADER([config.h])

# Checks for programs.
AC_DISABLE_STATIC
AC_PROG_LIBTOOL
AC_PROG_CC

AH_TOP([#include "xorg-server.h"])

PKG_PROG_PKG_CONFIG([0.25])
PKG_CHECK_MODULES(XORG, xorg-server xproto)
inputdir=`$PKG_CONFIG --variable=input_drivers_dir xorg-server`
AC_SUBST(inputdir)

# Checks for header files.
AC_HEADER_STDC

XORG_MANPAGE_SECTIONS
XORG_RELEASE_VERSION

AC_OUTPUT([Makefile src/Makefile man/Makefile])
