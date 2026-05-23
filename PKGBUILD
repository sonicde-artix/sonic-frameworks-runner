# Maintainer: artist for Artix Linux

pkgname=sonic-frameworks-runner
pkgver=6.26.0
pkgrel=1
pkgdesc='Framework for providing different actions given a string query'
arch=(x86_64)
url="https://github.com/Sonic-DE/$pkgname"
license=(LGPL-2.0-only LGPL-3.0-only)
depends=(libstdc++
         kconfig
         ki18n
         kitemmodels
         libgcc
         qt6-base
         sonic-frameworks-core-addons
         sonic-frameworks-windowsystem)
makedepends=(doxygen
             extra-cmake-modules
             kdoctools
             qt6-tools)
groups=(sonicde-frameworks)
conflicts=(krunner)
provides=(krunner)
replaces=(krunner)
source=("$pkgname-$pkgver.tar.gz::${url}/archive/refs/tags/$pkgver.tar.gz")

build() {
  cmake -B build -S $pkgname-$pkgver \
    -DBUILD_TESTING=OFF
  cmake --build build
}

package() {
  DESTDIR="$pkgdir" cmake --install build
}
sha256sums=('f83d4c28ca070ed3d9d483c70ddad85e9bfaa914bce52a19d7f2ae03234350ce')
