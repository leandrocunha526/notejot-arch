# Maintainer: Leandro Cunha <leandrocunha016@gmail.com>

pkgname=notejot
pkgver=3.3.3
pkgrel=1
pkgdesc="Stupidly simple notes app"
arch=(x86_64)
url="https://github.com/lainsce/notejot"
license=(GPL)
depends=(gtk4 libportal-gtk4 libadwaita)
makedepends=(json-glib git libgee meson vala gtk4 libportal-gtk4 libadwaita)
groups=(gnome-extra)
source=(
  "notejot::git+https://github.com/lainsce/notejot.git#tag=$pkgver"
)
sha256sums=("SKIP")
prepare() {
  cd $pkgname
}

build() {
  arch-meson $pkgname build
  meson compile -C build
}

package() {
  DESTDIR="$pkgdir" ninja -C build install
}

