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

CONFIGURE_ARGS += \
	--enable-shared \
	--enable-static \

$(eval $(call BuildPackage,librabbitmq))
