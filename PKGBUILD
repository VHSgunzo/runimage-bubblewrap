# Maintainer: VHSgunzo <vhsgunzo.github.io>

pkgname='runimage-bubblewrap'
pkgver='0.11.0.1'
pkgrel='1'
pkgdesc='Patched bubblewrap for RunImage container'
url='https://github.com/VHSgunzo/bubblewrap-static'
arch=('x86_64' 'aarch64')
license=('MIT')
options=(!strip)
provides=("bubblewrap=$pkgver-$pkgrel")
conflicts=('bubblewrap' 'bubblewrap-suid')
depends=('runimage-static')
source=("$url/releases/download/v$pkgver/bwrap-${CARCH}")
sha256sums=('SKIP')

package() {
  install -Dm755 "bwrap-${CARCH}" "${pkgdir}/var/RunDir/sharun/bin/bwrap"
  mkdir -p "${pkgdir}/usr/bin"
  ln -sr "${pkgdir}/var/RunDir/sharun/bin/bwrap" "${pkgdir}/usr/bin/bwrap"
}
