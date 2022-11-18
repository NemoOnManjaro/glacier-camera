# $Id$
# Contributor: TheKit <nekit1000 at gmail.com>
# Contributor: Bart Ribbers <bribbers@disroot.org>
# Contributor: Alexey Andreyev <aa13q@ya.ru>
# Maintainer: James Kittsmiller (AJSlye) <james@nulogicsystems.com>

pkgname=glacier-camera
pkgver=0.1.5
pkgrel=1
pkgdesc="Glacier Camera"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-camera"
license=('LGPL-2.0-or-later')
depends=('qt5-glacier-app>=0.9' 'nemo-qml-plugin-settings')
makedepends=('qt5-tools' 'cmake')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('44bb9c2e811ebc5d1292f9cf7e0346cc33ec3d03ea966c03a7a1bf7c03f41d4b')

build() {
    cd $pkgname-$pkgver
    cmake \
        -DCMAKE_INSTALL_PREFIX:PATH='/usr'
    make  all
}

package() {
    cd $pkgname-$pkgver
    make DESTDIR="$pkgdir" install
}
