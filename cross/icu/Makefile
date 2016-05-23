PKG_NAME = icu
PKG_VERS_MAJOR = 57
PKG_VERS_MINOR = 1
PKG_EXT = tgz
PKG_DIST_NAME = $(PKG_NAME)4c-$(PKG_VERS_MAJOR)_$(PKG_VERS_MINOR)-src.$(PKG_EXT)
PKG_DIST_SITE = http://download.icu-project.org/files/icu4c/$(PKG_VERS_MAJOR).$(PKG_VERS_MINOR)
PKG_DIR = $(PKG_NAME)/source

DEPENDS = native/icu

HOMEPAGE = http://site.icu-project.org
COMMENT  = ICU is a cross-platform Unicode based globalization library.
LICENSE  = http://source.icu-project.org/repos/icu/icu/tags/release-57-1/LICENSE

GNU_CONFIGURE = 1
CONFIGURE_ARGS = --enable-static --with-cross-build="$(WORK_DIR)/../../../native/$(PKG_NAME)/work-native/$(PKG_DIR)"

ADDITIONAL_CFLAGS = -O3
ADDITIONAL_CXXFLAGS = -O3

POST_INSTALL_TARGET = myPostInstall

include ../../mk/spksrc.cross-cc.mk

.PHONY: myPostInstall
myPostInstall:
	sed -i -e 's|^prefix=$$|prefix=$(STAGING_INSTALL_PREFIX)|' $(STAGING_INSTALL_PREFIX)/bin/icu-config

