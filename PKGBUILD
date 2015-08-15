# $Id: PKGBUILD 91845 2013-05-28 17:24:37Z spupykin $
# Maintainer: Sergej Pupykin <pupykin.s+arch@gmail.com>
# Contributor: Sergej Pupykin <pupykin.s+arch@gmail.com>

pkgname=checkinstall
pkgver=1.6.2
pkgrel=3
pkgdesc="spy for 'make install' and build rpm or deb"
arch=('i686' 'x86_64')
url="http://asic-linux.com.mx/~izto/checkinstall/"
license=('GPL')
backup=(etc/checkinstall/checkinstallrc)
source=(http://asic-linux.com.mx/~izto/checkinstall/files/source/$pkgname-$pkgver.tar.gz
	build-fix.patch)
md5sums=('d7b43c92001e68243a93bcce8b1e5480'
         'eac0c843781c300e7bc15c55be262e51')

build() {
  cd $srcdir/$pkgname-$pkgver
  patch -Np1 <../build-fix.patch
  make
}

package() {
  cd $srcdir/$pkgname-$pkgver
  make DESTDIR=$pkgdir install
}
