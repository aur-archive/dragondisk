# Contributor: Michael Louis Thaler <michael.louis.thaler@gmail.com>
# Maintainer: Michael Louis Thaler <michael.louis.thaler@gmail.com>
pkgname=dragondisk
pkgver=1.0.5
pkgrel=1
pkgdesc="DragonDisk, a free-as-in-beer Amazon S3 GUI client"
arch=(i686 x86_64)
url="http://www.dragondisk.com/"
license=('custom')
depends=(qt4 libstdc++5 zlib openssl)
makedepends=()

if [ "$CARCH" == i686 ]; then
  source=("http://download.dragondisk.com/dragondisk_$pkgver-0ubuntu_i386.deb")
  sha256sums=('bee5e3c578d89af2104db48ef360911aee8487e94be9cd48732c09224c699195')
elif [ "$CARCH" == x86_64 ]; then
  source=("http://download.dragondisk.com/dragondisk_$pkgver-0ubuntu_amd64.deb")
  sha256sums=('c6f6bfd23e6582191274c04438f3f3af5308f1c5afc998f4c23efe72c4bcccb0')
fi

package() {
  cd "$srcdir" || exit 1
  tar -xvf data.tar.gz

  install -D -m755 "$srcdir/usr/bin/dragondisk" "$pkgdir/usr/bin/dragondisk"

  install -D -m644 "$srcdir/usr/share/applications/dragondisk.desktop" "$pkgdir/usr/share/applications/dragondisk.desktop"
  install -D -m644 "$srcdir/usr/share/doc/dragondisk/changelog.Debian.gz" "$pkgdir/usr/share/doc/dragondisk/changelog.Debian.gz"
  install -D -m644 "$srcdir/usr/share/doc/dragondisk/copyright" "$pkgdir/usr/share/licenses/dragondisk/LICENSE"
  install -D -m644 "$srcdir/usr/share/pixmaps/dragondisk.xpm" "$pkgdir/usr/share/pixmaps/dragondisk.xpm"

}

# vim:set ts=2 sw=2 et:
