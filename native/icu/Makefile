PKG_NAME = icu
PKG_VERS_MAJOR = 57
PKG_VERS_MINOR = 1
PKG_EXT = tgz
PKG_DIST_NAME = $(PKG_NAME)4c-$(PKG_VERS_MAJOR)_$(PKG_VERS_MINOR)-src.$(PKG_EXT)
PKG_DIST_SITE = http://download.icu-project.org/files/icu4c/$(PKG_VERS_MAJOR).$(PKG_VERS_MINOR)
PKG_DIR = $(PKG_NAME)/source

DEPENDS =

HOMEPAGE = http://site.icu-project.org
COMMENT  = ICU is a cross-platform Unicode based globalization library.
LICENSE  = http://source.icu-project.org/repos/icu/icu/tags/release-57-1/LICENSE

GNU_CONFIGURE = 1
CONFIGURE_ARGS = --enable-static

ADDITIONAL_CFLAGS = -O3
ADDITIONAL_CXXFLAGS = -O3

include ../../mk/spksrc.native-cc.mk
