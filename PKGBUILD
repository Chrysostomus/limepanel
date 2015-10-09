
# Maintainer: Chrysostomus

pkgname=limepanel
_ver=0.1
pkgver=0.1.r64.91e6036
pkgrel=1
pkgdesc="i3 style panelfor bspwm using patched dmenu and lemonbar"
arch=any
url=https://github.com/Chrysostomus/limepanel
license=MIT
depends=('dmenu-manjaro'
	'lemonbar'
	'xdotool'
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
source="git://github.com/Chrysostomus/lemonpanel"
md5sums=('SKIP')

pkgver() {
	cd $pkgname
	printf "$_ver.r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package () {
	cd $srcdir
	install -Dm755 $srcdir/$pkgname/lemonpanel $pkgdir/usr/bin/lemonpanel
	cp -r $srcdir/$pkgname/bin $pkgdir/usr
	chmod a+x $pkgdir/usr/bin/*
}
