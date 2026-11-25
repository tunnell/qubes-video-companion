# Build and install the package from a checkout (the Qubes builder does not use this file)
VERSION := $(file <../version)
REL := $(file <../rel)
NVR := qubes-video-companion-$(VERSION)-$(REL)

package:
	sed "s/@VERSION@/$(VERSION)/;s/@REL@/$(REL)/" PKGBUILD.in > PKGBUILD
	git -C .. archive --prefix=$(NVR)/ -o archlinux/$(NVR).tar.gz HEAD
	makepkg -sfi
