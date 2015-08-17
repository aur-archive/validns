# Maintainer: kusakata <shohei atmark kusakata period com>

pkgname=validns
pkgver=0.8
pkgrel=1
pkgdesc="A high performance DNS/DNSSEC zone validator"
url="http://www.validns.net/"
license=('custom')
arch=('i686' 'x86_64')
depends=('judy' 'openssl')
source=("http://www.validns.net/download/validns-${pkgver}.tar.gz")

build() {
  cd "${srcdir}/validns-${pkgver}"
  
  make
}

package() {
  cd "${srcdir}/validns-${pkgver}"

  install -dm755 "${pkgdir}/usr/bin"
  install -m755 validns "${pkgdir}/usr/bin"

  install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}

md5sums=('3de6669b1c8794b21c25425d22215a9d')
