# $Id$
# Contributor: TheKit <nekit1000 at gmail.com>
# Contributor: Bart Ribbers <bribbers@disroot.org>
# Contributor: Alexey Andreyev <aa13q@ya.ru>
# Maintainer: James Kittsmiller (AJSlye) <james@nulogicsystems.com>

pkgname=glacier-camera
pkgver=0.1.4
pkgrel=1
pkgdesc="Glacier Camera"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-camera"
license=('LGPL-2.0-or-later')
depends=('qt5-glacier-app' 'nemo-qml-plugin-settings')
makedepends=('qt5-tools' 'cmake')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('0449003d49c6d4c76206be67a2e9b59149e0db7185f8e56a5b937303db291b1a')

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
