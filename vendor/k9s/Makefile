include ../../tasks/Makefile.vendor_includes

ifeq ($(ARCH), amd64)
	ARCH=x86_64
endif

ifeq ($(OS), darwin)
  OS=Darwin
else
  OS=Linux
endif

export VENDOR = derailed
export PACKAGE_NAME = k9s
export PACKAGE_REPO_NAME = k9s
export DOWNLOAD_URL = $(PACKAGE_REPO_URL)/releases/download/v$(PACKAGE_VERSION)/$(PACKAGE_NAME)_$(OS)_$(ARCH).tar.gz

## APK build specific requirements
export APK_BUILD_TEMPLATE = APKBUILD.github-binary

install:
	$(call download_tarball)

test:
	$(PACKAGE_EXE) version
