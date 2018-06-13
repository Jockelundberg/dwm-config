pkgname=dwm
pkgver=6.1
pkgrel=1
epoch=
pkgdesc=""
arch=('x86_64')
url="dwm.suckless.org"
license=('MIT')
groups=()
depends=('libx11' 'xorgproto' 'libxinerama' 'libxft' 'fontconfig' 'freetype2' 'st' 'dmenu')
makedepends=('git')
checkdepends=()
optdepends=()
provides=('dwm')
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("https://dl.suckless.org/$pkgname/$pkgname-$pkgver.tar.gz"
        "my_changes.diff")
noextract=()
sha256sums=('c2f6c56167f0acdbe3dc37cca9c1a19260c040f2d4800e3529a21ad7cce275fe'
            'SKIP')
validpgpkeys=()

prepare() {
	cd "$pkgname-$pkgver"
	patch < ../my_changes.diff
}

build() {
	cd "$pkgname-$pkgver"
	make clean all
}

package() {
	cd "$pkgname-$pkgver"
	make DESTDIR="$pkgdir/" install
}
