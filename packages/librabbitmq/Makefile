#
#
#
#

include $(TOPDIR)/rules.mk

PKG_NAME:=librabbitmq
PKG_VERSION:=0.0.1
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)_$(PKG_VERSION).hg216.orig.tar.gz
PKG_SOURCE_URL:=http://localhost/dl

include $(INCLUDE_DIR)/package.mk

define Package/librabbitmq
	SECTION:=base
	CATEGORY:=Libraries
	TITLE:=librabbitmq is a client library for RabbitMQ written in C
endef

define Build/Configure
	$(call Build/Configure/Default)
endef

define Build/InstallDev
  $(INSTALL_DIR) $(1)/usr/include
	$(CP) $(PKG_INSTALL_DIR)/usr/include/* $(1)/usr/include/
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/*.{a,so} $(1)/usr/lib/
endef
				
define Package/librabbitmq/install
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/*.so.* $(1)/usr/lib/	
endef

$(eval $(call BuildPackage,librabbitmq))
