# $Id$
# Contributor: TheKit <nekit1000 at gmail.com>
# Contributor: Bart Ribbers <bribbers@disroot.org>
# Contributor: Alexey Andreyev <aa13q@ya.ru>
# Maintainer: James Kittsmiller (AJSlye) <james@nulogicsystems.com>

pkgname=glacier-camera
pkgver=0.2
pkgrel=2
pkgdesc="Glacier Camera"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-camera"
license=('LGPL-2.0-or-later')
depends=('qt6-glacier-app>=0.9' 'nemo-qml-plugin-settings')
makedepends=('qt6-tools' 'clang' 'cmake')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('4842220c47c991231b51afe328289264fd5aecfc48bcf7d212a7782aad032e40')

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
