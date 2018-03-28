#
# Copyright (C) 2018 shoutr labs UG (haftungsbeschraenkt)
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=cciss_vol_status
PKG_VERSION:=1.12
PKG_RELEASE:=1

PKG_SOURCE_URL:=https://downloads.sourceforge.net/project/cciss/cciss_vol_status/
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_MD5SUM:=83cbd9907efeff48eb30e2a3ca89faa5

PKG_MAINTAINER:=Christian Beier <cb@shoutrlabs.com>

PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk

define Package/cciss-vol-status
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=A tool to show the status of logical drives attached to HP Smartarray controllers
  URL:=http://cciss.sourceforge.net
endef

define Package/cciss-vol-status/description
 A tool to show the status of logical drives attached to HP Smartarray controllers.
endef

define Package/cciss-vol-status/install
	$(INSTALL_DIR) $(1)/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/cciss_vol_status $(1)/bin/cciss-vol-status
endef

$(eval $(call BuildPackage,cciss-vol-status))
