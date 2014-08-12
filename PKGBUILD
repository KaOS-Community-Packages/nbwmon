pkgname=nbwmon
pkgver=0.3.1
pkgrel=1
pkgdesc="ncurses bandwidth monitor"
arch=('x86_64')
url="https://github.com/defer-/nbwmon"
license=('custom:MIT/X')
depends=('ncurses')
source=("https://github.com/defer-/$pkgname/archive/$pkgver.tar.gz")
sha1sums=('765ed9d01f01417b9ebb2cad03a4a79927c934f4')

build() {
	  cd "$pkgname-$pkgver"
	  make
}

package() {
	  cd "$pkgname-$pkgver"
	  make DESTDIR="$pkgdir/" install
	  install -Dm644 README "$pkgdir/usr/share/doc/$pkgname/README"
	  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

