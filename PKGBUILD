pkgname=norman-git
_gitname=norman
pkgver=git
pkgrel=1
pkgdesc="The Norman Keyboard Layout created by David Norman."
url="https://normanlayout.info"
arch=('any')
license=('unknown')
depends=('')
source=("git://github.com/deekayen/norman.git")
sha256sums=('SKIP')

pkgver() {
  cd $_gitname
  echo $(git rev-list --count HEAD).$(git rev-parse --short HEAD)
}

package() {
  cd ${srcdir}/${_gitname}/xorg/
  install -Dm644 norman  ${pkgdir}/usr/share/X11/xkb/symbols/workman
}
