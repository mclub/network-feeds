#
# Copyright (c) 
#
# This is free software
# See src/LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=udpintcp
PKG_VERSION:=20160624
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/rssnsj/udpintcp
PKG_SOURCE_VERSION:=4256b80
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_SOURCE_VERSION).tar.xz

PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE
PKG_MAINTAINER:=

PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)-$(PKG_VERSION)

PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk

define Package/udpintcp
  CATEGORY:=Network
  TITLE:=UDP in TCP Tunneller
  URL:=https://github.com/mclub/network-feeds
  MAINTAINER:=Unknown
endef

# define Build/Compile
# 	$(MAKE) -C $(PKG_BUILD_DIR)/src CC="$(TARGET_CROSS)gcc" \
# 		CFLAGS="$(TARGET_CPPFLAGS) $(TARGET_CFLAGS)"
# endef

define Package/udpintcp/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/ut-client $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/ut-server $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/ut-bridge $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/ut-bridge.mask $(1)/usr/bin
endef

$(eval $(call BuildPackage,udpintcp))