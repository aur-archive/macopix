# Maintainer: Thomas Dziedzic < gostrc at gmail >
# Contributor: ruinevil <ruinevil@gmail.com>

pkgname=macopix
pkgver=1.7.4
pkgrel=2
pkgdesc='Mascot Constructive Pilot for X'
arch=('i686' 'x86_64')
url='http://rosegray.sakura.ne.jp/macopix/index-e.html'
license=('GPL')
depends=('gtk2' 'glib2' 'libpng' 'openssl' 'libjpeg' 'libtiff' 'gdk-pixbuf' 'cairo' 'pango')
source=("http://rosegray.sakura.ne.jp/macopix/${pkgname}-${pkgver}.tar.bz2")
md5sums=('dee0d3ad046891bd6ec8c0d01d631bb5')

build() {
  cd ${pkgname}-${pkgver}

  LDFLAGS+=' -lX11' ./autogen.sh \
    --prefix=/usr

  make
}

package() {
  cd ${pkgname}-${pkgver}

  make DESTDIR=${pkgdir} install
}
