#
# Copyright (C) 2015 The LuCI Team <luci@lists.subsignal.org>
#
# This is free software, licensed under the GNU General Public License v2.
#

include $(TOPDIR)/rules.mk

LUCI_TITLE:=Fwknopd config - web config for the firewall knock daemon
LUCI_DEPENDS:=+luci-base +fwknopd +qrencode
PKG_LICENSE:=GPL-2.0
PKG_MAINTAINER:=Jonathan Bennett <JBennett@incomsystems.biz>

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
