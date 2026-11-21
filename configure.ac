dnl SPDX-License-Identifier: MIT OR X11
dnl
dnl Copyright © 2026 Enrico Weigelt, metux IT consult <info@metux.net>
AC_PREREQ(2.57)
AC_INIT([xlibre-xf86-input-egalax],
        25.0.0,
        [https://github.com/X11Libre/xf86-input-egalax/issues])

XLIBRE_INIT_MODULE_AM(egalax)

# Newer xorg-server.m4 defines this too; keep it for older SDKs.
version_suffix=`echo "$PACKAGE_VERSION" | sed 's/^[[^-]]*//'`
AC_DEFINE_UNQUOTED([PACKAGE_VERSION_SUFFIX], ["$version_suffix"],
                   [Pre-release suffix of the version])

AC_CONFIG_FILES([Makefile src/Makefile man/Makefile man/egalax.man])
AC_OUTPUT
