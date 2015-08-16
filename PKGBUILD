# Contributor: bender02 at gmx dot com
pkgname=nettle
pkgver=2.1
pkgrel=1
pkgdesc="A low-level cryptographic library"
arch=('i686' 'x86_64')
url="http://www.lysator.liu.se/~nisse/nettle/"
license=('GPL2')
install=nettle.install
source=(http://www.lysator.liu.se/~nisse/archive/$pkgname-$pkgver.tar.gz)
md5sums=('2bfaf16234a5d8deb96cd23f53a682bb')

build() {
  cd "$srcdir/$pkgname-$pkgver"

  ./configure --prefix=/usr --enable-shared
  make
  make check
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make DESTDIR="$pkgdir/" install
  rm $pkgdir/usr/share/info/dir
}

# vim:set ts=2 sw=2 et:
