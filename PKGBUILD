# Maintainer: hbdee <hbdee.arch@gmail.com>

pkgname=kdeplasma-applet-time-keeper
_pname=timekeeper
pkgver=0.3
pkgrel=2
pkgdesc="This plasmoid provides a clock and a calendar function via steampunk interface."
arch=(any)
url="http://kde-apps.org/content/show.php?content=159345"
license=('GPL')
depends=('kdebase-workspace' 'kdeedu-marble')
makedepends=('unzip')
conflicts=('kdeplasma-applet-time-keeper')
source=(http://kde-apps.org/CONTENT/content-files/159345-${_pname}-${pkgver}.plasmoid)
md5sums=('e1dccf9afa91e4d6f3cc99a1f973153c')

build() {
  unzip -o -q "$srcdir/159345-${_pname}-${pkgver}.plasmoid" -d "$srcdir/${_pname}"
  install -D $srcdir/${_pname}/metadata.desktop ${pkgdir}/"`kde4-config --prefix`/share/kde4/services/${_pname}.desktop"
  chmod -R 755 $srcdir/${_pname}/
  mkdir -p ${pkgdir}/"`kde4-config --prefix`/share/apps/plasma/plasmoids/${_pname}"
  cp -r $srcdir/${_pname}/* ${pkgdir}/"`kde4-config --prefix`/share/apps/plasma/plasmoids/${_pname}/"
}
 
