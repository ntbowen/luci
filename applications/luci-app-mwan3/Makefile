#
# Copyright (C) 2017 Dan Luedtke <mail@danrl.com>
#
# This is free software, licensed under the GNU General Public License v2.

include $(TOPDIR)/rules.mk

LUCI_TITLE:=LuCI support for the MWAN3 MultiWAN Manager
LUCI_DEPENDS:=+luci-base +mwan3
PKG_LICENSE:=GPL-2.0

PKG_MAINTAINER:=Florian Eckert <fe@dev.tdt.de>

include ../../luci.mk

define Package/$(PKG_NAME)
  SECTION:=$(LUCI_SECTION)
  CATEGORY:=$(LUCI_CATEGORY)
  SUBMENU:=$(LUCI_SUBMENU)
  TITLE:=$(if $(LUCI_TITLE),$(LUCI_TITLE),LuCI $(LUCI_NAME) $(LUCI_TYPE))
  DEPENDS:=$(LUCI_DEPENDS)
  VERSION:=$(if $(PKG_VERSION),$(if $(PKG_RELEASE),$(PKG_VERSION)-r$(PKG_RELEASE),$(PKG_VERSION)),$(PKG_SRC_VERSION))
  $(if $(LUCI_PKGARCH),PKGARCH:=$(LUCI_PKGARCH))
  URL:=$(LUCI_URL)
  MAINTAINER:=$(LUCI_MAINTAINER)
  HIDDEN:=1
endef

# call BuildPackage - OpenWrt buildroot signature
