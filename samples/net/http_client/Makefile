#
# Copyright (c) 2017 Intel Corporation
#
# SPDX-License-Identifier: Apache-2.0
#

BOARD ?= qemu_x86
CONF_FILE ?= prj.conf

include $(ZEPHYR_BASE)/Makefile.inc

ifeq ($(CONFIG_NET_L2_BT),y)
	QEMU_EXTRA_FLAGS = -serial unix:/tmp/bt-server-bredr
else
	include $(ZEPHYR_BASE)/samples/net/common/Makefile.ipstack
endif

SRC = $(ZEPHYR_BASE)/samples/net/http_client/src
include $(ZEPHYR_BASE)/scripts/Makefile.gen
