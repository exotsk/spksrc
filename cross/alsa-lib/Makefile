PKG_NAME = alsa-lib
PKG_VERS = 1.1.2
PKG_EXT = tar.bz2
PKG_DIST_NAME = $(PKG_NAME)-$(PKG_VERS).$(PKG_EXT)
PKG_DIST_SITE = ftp://ftp.alsa-project.org/pub/lib
PKG_DIR = $(PKG_NAME)-$(PKG_VERS)

DEPENDS =

HOMEPAGE = https://www.alsa-project.org/
COMMENT  = Advanced Linux Sound Architecture provides audio and MIDI functionality to the Linux operating system
LICENSE  = LGPLv2.1

GNU_CONFIGURE = 1
CONFIGURE_ARGS = --disable-python
ifeq ($(findstring $(ARCH), ppc853x ppc854x),$(ARCH))
ADDITIONAL_CFLAGS = -DNO_TLS_PFX
endif

INSTALL_TARGET = alsa-lib_install

include ../../mk/spksrc.cross-cc.mk

.PHONY: alsa-lib_install
alsa-lib_install:
	$(RUN) make install DESTDIR=$(INSTALL_DIR)
