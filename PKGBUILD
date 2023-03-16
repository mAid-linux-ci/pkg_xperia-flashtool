# Maintainer: xstefen <me@xstefen.dev>
# Contributor: BrLi <hidden>
# Contributor: philacs <yue.liu@mail.com>

pkgname=xperia-flashtool
_realname=flashtool
pkgver=0.9.36.0
pkgrel=2
pkgdesc="A S1 protocol flashing software for Sony Xperia phones"
arch=('x86_64')
url="http://www.flashtool.net/"
license=('GPL3')
depends=('libselinux' 'libsystemd' 'glib2' 'mono')
# ${source} obtained from upstream project ${url}
source=("https://github.com/Androxyde/Flashtool/releases/download/${pkgver}/${_realname}-${pkgver}.tar.bz2"
        "${pkgname}.sh")
# Upstream archive and launcher script
md5sums=('d45dcd8fb36500e8dec05cbf939b1d0e'
         '457c5decbc0f5ace3d0d9b98dfdd9ffa')
options=('!strip')

package() {
  # Install program files
  install -m 755 -d "${pkgdir}/usr/lib/${pkgname}"
  cp -rt "${pkgdir}/usr/lib/${pkgname}" Flashtool/*
  # Install launcher scripts
  install -m 755 -d "${pkgdir}/usr/bin"
  install -m 755 "${pkgname}.sh" "${pkgdir}/usr/bin/${pkgname}"
}
