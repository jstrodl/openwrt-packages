include $(TOPDIR)/rules.mk
 
PKG_NAME:=quectel-cm
PKG_VERSION:=aa24eb5
PKG_RELEASE:=1

PKG_MAINTAINER:=Johannes Strodl <johannes.strodl@gmail.com>
PKG_LICENSE:=LGPL-3.0-or-later
PKG_LICENSE_FILES:=COPYING
 
PKG_SOURCE:=jstrodl-quectel-cm-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/jstrodl/quectel-cm/tarball/$(PKG_VERSION)
PKG_HASH:=612ad834f9a883e1e0b5fca49153ee60f391fdd4cf0f991144bafe2a64b7433c

PKG_BUILD_DIR:=$(BUILD_DIR)/jstrodl-quectel-cm-$(PKG_VERSION)
PKG_FIXUP:=autoreconf
MAKE_PATH:=src
 
include $(INCLUDE_DIR)/package.mk
 
define Package/quectel-cm
	SECTION:=net
	CATEGORY:=Network
	SUBMENU:=WWAN
	TITLE:=Quectel modem connection utility
	URL:=https://github.com/jstrodl/quectel-cm
endef
 
define Package/quectel-cm/description
	Connectivity control utility for Quectel UMTS/HSPA/LTE modems.
endef

#define Build/Configure
#	$(call Build/Configure/Default,)
#endef

#define Build/Compile
#	rm -rf $(PKG_INSTALL_DIR)
#	mkdir -p $(PKG_INSTALL_DIR)
#endef
 
define Package/quectel-cm/install
	$(INSTALL_DIR) $(1)/usr/sbin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/src/quectel_cm $(1)/usr/sbin/
endef
 
$(eval $(call BuildPackage,quectel-cm))
