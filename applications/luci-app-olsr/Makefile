#
# Copyright (C) 2008-2014 The LuCI Team <luci@lists.subsignal.org>
#
# This is free software, licensed under the Apache License, Version 2.0 .
#

include $(TOPDIR)/rules.mk

LUCI_TITLE:=OLSR configuration and status module
LUCI_DEPENDS:=+luci-base +olsrd +olsrd-mod-jsoninfo +olsrd-mod-sgwdynspeed

PKG_LICENSE:=Apache-2.0
PKG_MAINTAINER:=Manuel Munz <munz@comuno.net>

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
