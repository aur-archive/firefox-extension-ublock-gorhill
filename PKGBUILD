 # Maintainer: ThePierrezou <thepierrezou@openmailbox.org>
# Contributor: polyzen <polycitizen@gmail.com>

pkgname=firefox-extension-ublock-gorhill
pkgver=0.9.9.1
pkgrel=1
pkgdesc='Finally, an efficient blocker. Easy on CPU and memory. Gorhill version.'
url=https://github.com/gorhill/uBlock
arch=('any')
license=('GPL3')
depends=('firefox')
conflicts=('firefox-extension-ublock-gorhill-git' 'firefox-ublock-origin' )
source=("https://github.com/gorhill/uBlock/releases/download/$pkgver/uBlock0.firefox.xpi")

package() {
  local GLOBIGNORE=*.xpi:LICENSE.txt
  local version="$(grep -Pom1 '(?<=<id>).*(?=</id>)' install.rdf)"
  local dstdir="$pkgdir/usr/lib/firefox/browser/extensions/$version"
  install -d "$dstdir"
  cp -dpr --no-preserve=ownership * "$dstdir"
  chmod -R 755 "$dstdir"
}

# vim:set ts=2 sw=2 et:
sha256sums=('6e1c5df569d00206ee2f745c2d3193e052a57de6a60e4299c7464892866b0bca')

