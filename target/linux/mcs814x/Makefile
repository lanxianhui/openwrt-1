#
# Copyright (C) 2012 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#
include $(TOPDIR)/rules.mk

ARCH:=arm
BOARD:=mcs814x
BOARDNAME:=WRTnode Hi
FEATURES:=usb squashfs low_mem
CPU_TYPE:=arm926ej-s
MAINTAINER:=Florian Fainelli <florian@openwrt.org>

KERNEL_PATCHVER:=3.18

DEVICE_TYPE:=other

include $(INCLUDE_DIR)/target.mk

DEFAULT_PACKAGES := $(filter-out ppp%,$(DEFAULT_PACKAGES)) \
		  kmod-usb-core kmod-usb2 kmod-usb-ohci \
		  kmod-usb-storage kmod-fs-vfat \
		  kmod-nls-cp437 kmod-nls-iso8859-1 kmod-nls-iso8859-15 \
		  kmod-nls-utf8 \
		  kmod-mcs814x-wdt kmod-ledtrig-usbdev luci

KERNELNAME:=zImage dtbs

$(eval $(call BuildTarget))
