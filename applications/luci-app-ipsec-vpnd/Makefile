include $(TOPDIR)/rules.mk

LUCI_TITLE:=LuCI support for IPSec VPN Server (IKEv1 with PSK and Xauth)
LUCI_DEPENDS:=+strongswan +strongswan-minimal +strongswan-mod-xauth-generic +strongswan-mod-kernel-libipsec +kmod-tun
LUCI_PKGARCH:=all

define Package/luci-app-ipsec-vpnd/conffiles
/etc/config/ipsec-vpnd
endef

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
