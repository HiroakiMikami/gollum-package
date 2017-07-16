# Maintainer: Hiroaki Mikami <hiroaki8270@gmail.com>
pkgname=gollumd
pkgver=r1.f7821b1
pkgrel=1
pkgdesc=""
arch=("x86_64")
url=""
license=('unknown')
groups=()
provides=("${pkgname}")
conflicts=("${pkgname}")
replaces=()
backup=()
options=()
noextract=()

pkgver() {
  cd "$srcdir"

  # Git, no tags available
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
  # Add systemd service
  cd "$startdir"
  mkdir -p "$pkgdir/usr/local/bin"
  mkdir -p "$pkgdir/etc/systemd/user"
  cp ./gollumd "$pkgdir/usr/local/bin"
  cp ./gollumd@.service "$pkgdir/etc/systemd/user/"
}
