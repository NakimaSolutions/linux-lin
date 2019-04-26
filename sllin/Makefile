SHELL := /bin/bash
EXTRA_CFLAGS += $(USER_EXTRA_CFLAGS)
EXTRA_CFLAGS += -O1


SUBARCH := $(shell uname -m | sed -e "s/i.86/i386/; s/ppc/powerpc/; s/armv.l/arm/; s/aarch64/arm64/;")

ARCH ?= $(SUBARCH)
CROSS_COMPILE ?=
KVER := $(shell uname -r)
KSRC ?= /lib/modules/$(KVER)/build


export CONFIG_SLLIN = m
obj-$(CONFIG_SLLIN) := sllin.o

all: modules

modules:
	$(MAKE) ARCH=$(ARCH) CROSS_COMPILE=$(CROSS_COMPILE) -C $(KSRC) M=$(shell pwd)  modules

clean:
	$(MAKE) ARCH=$(ARCH) CROSS_COMPILE=$(CROSS_COMPILE) -C $(KSRC) M=$(shell pwd)  clean
	rm -fr .cache.mk *~
