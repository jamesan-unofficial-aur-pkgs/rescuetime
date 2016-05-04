# Maintainer: James An <james@jamesan.ca>
# Contributor: Limao Luo <luolimao+AUR@gmail.com>
# Contributor: kaptoxic

pkgname=rescuetime
pkgver=2.9.10.1255
pkgrel=3
pkgdesc="Application time-tracking for Linux. Stable version"
arch=('i686' 'x86_64')
url='https://www.rescuetime.com'
license=('GPL2')
depends=('qt4' 'xorg-xprop' 'xprintidle')
conflicts=("$pkgname-beta")
install=$pkgname.install
changelog=$pkgname.changelog
source_i686=("$url/installers/${pkgname}_current_i386.deb")
source_x86_64=("$url/installers/${pkgname}_current_amd64.deb")
md5sums_i686=('79ef7170b5e047712751fa769fd21465')
md5sums_x86_64=('bd81f31fbb13a5b73ac5bf41bbf243f6')

prepare() {
  bsdtar -xf data.tar.gz
}

package() {
    install -Dm755 usr/bin/$pkgname "$pkgdir"/usr/bin/$pkgname
    install -Dm644 usr/share/$pkgname/curl-ca-bundle.crt "$pkgdir"/usr/share/$pkgname/curl-ca-bundle.crt
}
