# Maintainer: Guillaume ALAUX <guillaume at alaux dot net>
_confname=us_qwerty_frcode
_appname="xkbmap_${_confname}"
pkgname=${_appname}-git
pkgver=r2.b049ed1
pkgrel=1
pkgdesc='An X keyboard configuration for US Qwerty, French accents and coding symbols'
arch=('any')
url="https://github.com/galaux/${_appname}"
license=('GPL')
makedepends=('git')
source=("${_appname}::git+${url}")
sha256sums=('SKIP')

pkgver() {
  cd "${srcdir}/${_appname}"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
  install -D -m 644 \
    "${srcdir}/${_appname}/${_confname}" \
    "${pkgdir}/usr/share/X11/xkb/symbols/${_confname}"
}
