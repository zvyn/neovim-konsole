# Maintainer: Milan Oberkirch <aur@oberkirch.org>
pkgname=neovim-konsole-git
pkgver=r23.8f82ad7
pkgrel=1
pkgdesc=""
arch=('any')
url="https://github.com/zvyn/neovim-konsole"
license=()
groups=()
depends=()
makedepends=('git')
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
source=("git+https://github.com/zvyn/neovim-konsole.git")
noextract=()
md5sums=('SKIP')

_gitname="neovim-konsole"

pkgver() {
  cd "$srcdir/$_gitname"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
  cd "$srcdir/$_gitname"
  mkdir --parents $pkgdir/usr/bin/
  mkdir --parents $pkgdir/usr/share/
  cp -v --parents -r share $pkgdir/usr/
  cp -v --parents -r konsole $pkgdir/usr/share/
  cp -v bin/nvim-konsole $pkgdir/usr/bin/nvim-konsole
}

# vim:set ts=2 sw=2 et:
