include ../../tasks/Makefile.vendor_includes

# Package details
export VENDOR ?= sahsanu
export APK_BUILD_TEMPLATE ?= APKBUILD.github-binary
export APKBUILD_DEPENDS += util-linux bash
export DEB_FPM_EXTRA_ARGS += --depends bsdmainutils
export OS_ARCH = noarch
export PACKAGE_DIST_ARCH = noarch
GITHUB_VERSION = $(shell echo $(PACKAGE_VERSION) | sed -E 's/\.0$$//')
export DOWNLOAD_URL ?= https://raw.githubusercontent.com/sahsanu/lectl/v$(GITHUB_VERSION)/lectl

install:
	$(call download_binary)

test:
	$(PACKAGE_EXE) --version
