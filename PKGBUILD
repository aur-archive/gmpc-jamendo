# Modified from original gmpc pkgbuild created by tobias <tobias@archlinux.org>
# Contributor: Lukas Miczka <lukascpu@gmail.com>

pkgname=gmpc-jamendo
pkgver=11.8.16
pkgrel=1
pkgdesc="The jamendo plugin allows you to browse and preview music available on jamendo."
arch=('i686' 'x86_64')
url="http://sarine.nl/gmpc/"
license=('GPL')
depends=("gmpc>=${pkgver}" "libmpd>=${pkgver}" "intltool>=0.21" "json-glib" "gob2")
options=('!libtool')
source=(http://download.sarine.nl/Programs/gmpc/${pkgver}/${pkgname}-${pkgver}.tar.gz)
sha1sums=('28c1bb336762740352f84a7710be51d259301324')

build() {
   cd "$pkgname-$pkgver"
   ./configure --prefix=/usr
   make
}
package() {
   cd "$pkgname-$pkgver"
   make DESTDIR=$pkgdir install
}

