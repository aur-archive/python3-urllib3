# Maintainer: Patrice Peterson <runiq at archlinux dot us>
# Contributor: Chris Brannon <cmbrannon79@gmail.com>

pkgname=python3-urllib3
_pkgname=urllib3
pkgver=1.5
pkgrel=1
pkgdesc="HTTP library with thread-safe connection pooling and file post support, Python 3 version"
arch=("any")
url="https://github.com/shazow/urllib3"
license=("MIT")
depends=("python")
makedepends=("python-distribute")
source=("${_pkgname}-${pkgver}.tar.gz::https://github.com/shazow/urllib3/tarball/1.5" 
        LICENSE)
md5sums=('d1ec8e2e01264f176e2361d5bbbf49a7'
         '350846ab4dd11ce105b570c15c1b0764')

package() {
  cd "$srcdir/shazow-${_pkgname}-f7eaa46"
  python setup.py install --root="${pkgdir}" --optimize=1
  install -Dm644 "${srcdir}/LICENSE" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
