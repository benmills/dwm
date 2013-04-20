# $Id: PKGBUILD 60970 2011-12-19 21:33:58Z spupykin $
# Maintainer: Sergej Pupykin <pupykin.s+arch@gmail.com>
# Contributor: Dag Odenhall <dag.odenhall@gmail.com>
# Contributor: Grigorios Bouzakis <grbzks@gmail.com>

pkgname=dwm
pkgver=6.0
pkgrel=1
pkgdesc="A dynamic window manager for X"
url="http://dwm.suckless.org"
arch=('i686' 'x86_64')
license=('MIT')
options=(zipman)
depends=('libx11' 'libxinerama')
install=dwm.install
source=(http://dl.suckless.org/dwm/dwm-$pkgver.tar.gz
	config.h
	dwm.desktop)
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '2453e037f46449774ec8afab49b4f1a2'
         '939f403a71b6e85261d09fc3412269ee')

build() {
  cd $srcdir/$pkgname-$pkgver
  cp $srcdir/config.h config.h
  sed -i 's/CPPFLAGS =/CPPFLAGS +=/g' config.mk
  sed -i 's/^CFLAGS = -g/#CFLAGS += -g/g' config.mk
  sed -i 's/^#CFLAGS = -std/CFLAGS += -std/g' config.mk
  sed -i 's/^LDFLAGS = -g/#LDFLAGS += -g/g' config.mk
  sed -i 's/^#LDFLAGS = -s/LDFLAGS += -s/g' config.mk
  make X11INC=/usr/include/X11 X11LIB=/usr/lib/X11
}

package() {
  cd $srcdir/$pkgname-$pkgver
  make PREFIX=/usr DESTDIR=$pkgdir install
  install -m644 -D LICENSE $pkgdir/usr/share/licenses/$pkgname/LICENSE
  install -m644 -D README $pkgdir/usr/share/doc/$pkgname/README
  install -m644 -D $srcdir/dwm.desktop $pkgdir/usr/share/xsessions/dwm.desktop
}
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '2453e037f46449774ec8afab49b4f1a2'
         '939f403a71b6e85261d09fc3412269ee')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '5905a957af3a45b56e2da9ebf70a14ca'
         '939f403a71b6e85261d09fc3412269ee')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '440ae799a604048440e1cf28685fc685'
         '939f403a71b6e85261d09fc3412269ee')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         'd37ab135d5c3bcc336ad0e56fff2bb48'
         '939f403a71b6e85261d09fc3412269ee')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '7ac5739e9dadc4139ed7852f451699f5'
         '939f403a71b6e85261d09fc3412269ee')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         'dba13b199cbfc2637eec5ba11083f17d'
         '939f403a71b6e85261d09fc3412269ee')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         'e4c4b7cad4c9a8899949dd29105a1ceb'
         '939f403a71b6e85261d09fc3412269ee')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         'e4c4b7cad4c9a8899949dd29105a1ceb'
         '939f403a71b6e85261d09fc3412269ee')
