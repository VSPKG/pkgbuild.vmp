# Maintainer: Vineel Sai <mail@vineelsai.com>
pkgname='vmp'
pkgver=v0.1.1
pkgrel=1
epoch=
pkgdesc="A Program to manage Python versions"
arch=("x86_64" "aarch64")
url="https://vineelsai.com"
license=('MIT')
groups=()
depends=()
makedepends=('git' 'cargo')
checkdepends=()
optdepends=()
provides=(vmp)
conflicts=()
replaces=()
backup=()
options=(!debug)
changelog=
source=("git+https://github.com/vineelsai26/$pkgname.git")
noextract=()
md5sums=('SKIP')
validpgpkeys=()

pkgver() {
    cd "$pkgname"
    printf "$(git describe --tags --abbrev=0)"
}

build() {
    cd "$pkgname"
    cargo build --verbose --release --all-features
}

package() {
	cd "$pkgname"
    install -Dm755 target/release/"$pkgname" "${pkgdir}/usr/bin/${pkgname}"
}
