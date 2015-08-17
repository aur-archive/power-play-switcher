# Maintainer: Julien Nicoulaud <julien.nicoulaud@gmail.com>
# Source: https://github.com/nicoulaj/archlinux-packages
pkgname=power-play-switcher
pkgver=0.3
pkgrel=2
pkgdesc="PowerPlay GUI for the open source ATI driver."
arch=(any)
url="http://code.google.com/p/power-play-switcher"
license=(GPL3)
depends=(python2 pygtk xf86-video-ati)
makedepends=(subversion)
install=power-play-switcher.install
changelog=Changelog
conflicts=(power-play-switcher-svn)
source=(http://${pkgname}.googlecode.com/files/PowerPlaySwitcher-${pkgver}.zip
        power-play-switcher.desktop)
md5sums=('3c475e7eed167985a75142a0838f6e8f'
         '3bb7a8b8cdcf199e4aa776f1503c88f3')

package() {

  msg2 "Fix Python script shebang..."
  sed -i -e 's/\#\!\/usr\/bin\/python/\#\!\/usr\/bin\/env\ python2/' "${srcdir}"/PowerPlaySwitcher.py

  msg2 "Install script at /usr/bin/power-play-switcher..."
  install -Dm755 "${srcdir}"/PowerPlaySwitcher.py "${pkgdir}"/usr/bin/power-play-switcher

  msg2 "Install desktop application entry..."
  install -Dm644 "${srcdir}"/power-play-switcher.desktop "${pkgdir}"/usr/share/applications/power-play-switcher.desktop

}

# vim:set ts=2 sw=2 et:
