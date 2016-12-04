pkgname=m17n-lib
pkgver=1.7.0
pkgrel=1
pkgdesc='Multilingual text processing library (runtimes)'
url='http://www.nongnu.org/m17n/'
arch=('x86_64')
license=('GPL')
depends=('libxft' 'm17n-db' 'fribidi' 'libxml2' 'gd' 'libotf')
source=("http://download.savannah.gnu.org/releases/m17n/${pkgname}-${pkgver}.tar.gz")
sha1sums=('6ebc98680ffb575c5f58190f054d60fdb8b0f301')

build() {
	cd "${srcdir}/${pkgname}-${pkgver}"
	./configure --prefix=/usr
	make
}

package() {
	cd "${srcdir}/${pkgname}-${pkgver}"
	make DESTDIR="${pkgdir}" install
}
