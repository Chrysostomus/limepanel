
# Maintainer: Bernhard Landauer <oberon@manjaro.org>
# Maintainer: Chrysostomus

pkgname=limepanel
_ver=0.7
pkgver=0.7.r79.db71adb
pkgrel=1
pkgdesc="Panel script for bspwm using patched dmenu and lemonbar"
arch=any
url=https://github.com/Chrysostomus/limepanel
license=MIT
depends=('dmenu-manjaro'
	'lemonbar-xft-clicky'
	'xdotool'
	'pulseaudio-ctl'
	'rxvt-unicode'
	'networkmanager-dmenu'
	'conky-cli'
	'xorg-xdpyinfo'
	'xtitle'
	'bdf-zevv-peep'
	'ttf-ionicons'
	'zenity'
	'xdg-utils')
makedepends=git
source="git://github.com/Chrysostomus/limepanel"
md5sums=('SKIP')

pkgver() {
	cd $pkgname
	printf "$_ver.r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package () {
	cd $srcdir/$pkgname
	install -dm755 $pkgdir/usr
	cp -r bin $pkgdir/usr
	chmod a+x $pkgdir/usr/bin/*
}
