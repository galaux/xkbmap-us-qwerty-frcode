# Maintainer: Guillaume ALAUX <guillaume at alaux dot net>
_confname=us_qwerty_frcode
_reponame="xkbmap-${_confname//_/-}"
pkgname=${_reponame}-git
pkgver=r10.526ab17
pkgrel=1
pkgdesc='An X keyboard configuration for US Qwerty, French accents and coding symbols'
arch=('any')
url="https://github.com/galaux/${_reponame}"
license=('GPL')
makedepends=('git')
source=("${_reponame}::git+${url}")
sha256sums=('SKIP')

pkgver() {
  cd "${srcdir}/${_reponame}"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
  install -D -m 644 \
    "${srcdir}/${_reponame}/${_confname}" \
    "${pkgdir}/usr/share/X11/xkb/symbols/${_confname}"
}
