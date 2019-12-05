pkgname=nbwmon
pkgver=0.5.2
pkgrel=1
pkgdesc="ncurses bandwidth monitor"
arch=('x86_64')
url="https://github.com/causes-/nbwmon"
license=('custom:MIT/X')
depends=('ncurses')
source=("https://github.com/causes-/$pkgname/archive/$pkgver.tar.gz")
sha512sums=('11502015b8a04d8a65c2f06d9e921c193c2e4968dbbd781791c30f35a2cf1135bbf784280b9070670be2b58c4355bf7bdf631d5932ec3a01637db803a4c88bf4')

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

