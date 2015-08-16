# Maintainer: Charles Bos <charlesbos1 AT gmail>
# Contributor: Xiao-Long Chen <chenxiaolong@cxl.epac.to>

pkgname=libcolumbus
_actual_ver=1.1.0
_extra_ver=+14.04.20140306
_source_date=20140306
pkgver=${_actual_ver}.${_source_date}
pkgrel=1
pkgdesc="A small, fast, error tolerant matcher"
arch=('i686' 'x86_64')
url="https://launchpad.net/libcolumbus"
license=('LGPL')
groups=('unity')
depends=('icu')
makedepends=('boost' 'cmake' 'sparsehash')
source=("https://launchpad.net/ubuntu/+archive/primary/+files/libcolumbus_${_actual_ver}${_extra_ver}.orig.tar.gz")
sha512sums=('a4aa3c94492f7d9ac0baefbeb3f8b030613a992b272224b3db65bd0b129d08ed23e902e7ef10ed5e213a0a238bf0cb7f93b8c861ac303c3a5a1e8e05e735eac7')

build() {
  cd "${srcdir}/${pkgname}-${_actual_ver}${_extra_ver}"
  mkdir build
  cd build
  cmake .. -DCMAKE_INSTALL_PREFIX=/usr -DCMAKE_BUILD_TYPE=''
  make
}

package() {
  cd "${srcdir}/${pkgname}-${_actual_ver}${_extra_ver}/build"
  make DESTDIR="${pkgdir}/" install
}

# vim:set ts=2 sw=2 et:
