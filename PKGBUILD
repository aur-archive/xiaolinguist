
# Maintainer: XIE Yuheng <xyheme@gmail.com>

pkgname=xiaolinguist
pkgver=20140531
pkgrel=1
epoch=
pkgdesc="xiaolinguist language"
arch=('x86_64')
url="https://bitbucket.org/xiaolinguist/xiaolinguist"
license=('ISC')
groups=()
depends=('fasm' 'mercurial')
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=('hg+https://bitbucket.org/xiaolinguist/xiaolinguist')
noextract=()
md5sums=('SKIP')

build() {
  cd "$srcdir/$pkgname/play"
  fasm -m 50000 xiaolinguist-core.fasm
}

package() {
  cp -rTn "$srcdir/$pkgname" "$HOME/xiaolinguist"
  install -D "$srcdir/$pkgname/play/xiaolinguist.sh" "$pkgdir/etc/profile.d/xiaolinguist.sh"
}
