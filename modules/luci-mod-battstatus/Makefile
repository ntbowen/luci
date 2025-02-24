include $(TOPDIR)/rules.mk

LUCI_TITLE:=Photonicat Battery Status
LUCI_DESCRIPTION:=Provides a battery charge indicator in LuCI. Currently only supports Photonicat.

LUCI_DEPENDS:=+luci-base +libiwinfo-lua +rpcd-mod-iwinfo +pcat-manager

PKG_LICENSE:=Apache-2.0

include ../../luci.mk

# Install CSS file
$(eval $(call LUCI_INSTALL_PRELOAD,battstatus,/www/luci-static/resources/preload,battstatus.css))

# call BuildPackage - OpenWrt buildroot signature
