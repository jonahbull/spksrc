ARCH ?= armada375
TCVERSION ?= 6.2
PKG_NAME = armada375
PKG_BRANCH = 22259
PKG_ARCH = $(PKG_NAME)
PKG_EXT = txz
PKG_DIST_NAME = linux-3.x.$(PKG_EXT)
PKG_DIST_SITE = https://downloads.sourceforge.net/project/dsgpl/Synology%20NAS%20GPL%20Source/$(PKG_BRANCH)branch/$(PKG_ARCH)-source
PKG_DIST_FILE = $(PKG_NAME)-$(PKG_DIST_NAME)
PKG_EXTRACT = linux-3.x
SYNO_CONFIG = synoconfigs/$(PKG_ARCH)
BASE_ARCH = arm

HOMEPAGE = http://www.synology.com/

PRE_COMPILE_TARGET = myPreCompile

include ../../mk/spksrc.kernel-modules.mk

PHONY: myPreCompile
myPreCompile:
	cd $(KERNEL_DIR)/arch/arm/ && rm -rf plat-armada && ln -s plat-armada-v2 plat-armada
