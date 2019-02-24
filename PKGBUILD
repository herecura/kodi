# vim:set ts=2 sw=2 et:
# Maintainer: Sergej Pupykin <pupykin.s+arch@gmail.com>
# Maintainer: BlackIkeEagle < ike DOT devolder AT gmail DOT com >
# Contributor: graysky <graysky AT archlinux DOT us>
# Contributor: DonVla <donvla@users.sourceforge.net>
# Contributor: Ulf Winkelvos <ulf [at] winkelvos [dot] de>
# Contributor: Ralf Barth <archlinux dot org at haggy dot org>
# Contributor: B & monty - Thanks for your hints :)
# Contributor: marzoul
# Contributor: Sergej Pupykin <pupykin.s+arch@gmail.com>
# Contributor: Brad Fanella <bradfanella@archlinux.us>
# Contributor: [vEX] <niechift.dot.vex.at.gmail.dot.com>
# Contributor: Zeqadious <zeqadious.at.gmail.dot.com>
# Contributor: Bartłomiej Piotrowski <bpiotrowski@archlinux.org>
# Contributor: Maxime Gauduin <alucryd@gmail.com>
#
# Original credits go to Edgar Hucek <gimli at dark-green dot com>
# for his xbmc-vdpau-vdr PKGBUILD at https://archvdr.svn.sourceforge.net/svnroot/archvdr/trunk/archvdr/xbmc-vdpau-vdr/PKGBUILD

pkgbase=kodi
pkgname=('kodi' 'kodi-eventclients' 'kodi-tools-texturepacker' 'kodi-dev')
pkgver=18.1
pkgrel=2
arch=('x86_64')
url="https://kodi.tv"
license=('GPL2')
makedepends=(
  'afpfs-ng' 'bluez-libs' 'cmake' 'curl' 'doxygen' 'glew'
  'gperf' 'hicolor-icon-theme' 'jasper' 'java-runtime' 'libaacs' 'libass'
  'libbluray' 'libcdio' 'libcec' 'libgl' 'mariadb-libs' 'libmicrohttpd'
  'libmodplug' 'libmpeg2' 'libnfs' 'libplist' 'libpulse' 'libssh' 'libva'
  'libvdpau' 'libxrandr' 'libxslt' 'lirc' 'lzo' 'mesa' 'nasm' 'nss-mdns'
  'python2-pillow' 'python2-pybluez' 'python2-simplejson' 'rtmpdump'
  'shairplay' 'smbclient' 'speex' 'swig' 'taglib' 'tinyxml' 'unzip' 'upower'
  'yajl' 'zip' 'git' 'giflib' 'rapidjson' 'ghostscript'
)

_codename=Leia

_libdvdcss_version="1.4.2-$_codename-Beta-5"
_libdvdnav_version="6.0.0-$_codename-Alpha-3"
_libdvdread_version="6.0.0-$_codename-Alpha-3"
_ffmpeg_version="4.0.3-$_codename-RC5"
_fmt_version="5.1.0"
_crossguid_version="8f399e8bd4"
_fstrcmp_version="0.7.D001"
_flatbuffers_version="1.9.0"

source=(
  "$pkgbase-$pkgver-$_codename.tar.gz::https://github.com/xbmc/xbmc/archive/$pkgver-$_codename.tar.gz"
  "$pkgbase-libdvdcss-$_libdvdcss_version.tar.gz::https://github.com/xbmc/libdvdcss/archive/$_libdvdcss_version.tar.gz"
  "$pkgbase-libdvdnav-$_libdvdnav_version.tar.gz::https://github.com/xbmc/libdvdnav/archive/$_libdvdnav_version.tar.gz"
  "$pkgbase-libdvdread-$_libdvdread_version.tar.gz::https://github.com/xbmc/libdvdread/archive/$_libdvdread_version.tar.gz"
  "$pkgbase-ffmpeg-$_ffmpeg_version.tar.gz::https://github.com/xbmc/FFmpeg/archive/$_ffmpeg_version.tar.gz"
  "$pkgbase-fmt-$_fmt_version.tar.gz::http://mirrors.kodi.tv/build-deps/sources/fmt-$_fmt_version.tar.gz"
  "$pkgbase-crossguid-$_crossguid_version.tar.gz::http://mirrors.kodi.tv/build-deps/sources/crossguid-$_crossguid_version.tar.gz"
  "$pkgbase-fstrcmp-$_fstrcmp_version.tar.gz::http://mirrors.kodi.tv/build-deps/sources/fstrcmp-$_fstrcmp_version.tar.gz"
  "$pkgbase-flatbuffers-$_flatbuffers_version.tar.gz::http://mirrors.kodi.tv/build-deps/sources/flatbuffers-$_flatbuffers_version.tar.gz"
  'cheat-sse-build.patch'
  'cpuinfo'
)
noextract=(
  "$pkgbase-libdvdcss-$_libdvdcss_commit.tar.gz"
  "$pkgbase-libdvdnav-$_libdvdnav_commit.tar.gz"
  "$pkgbase-libdvdread-$_libdvdread_commit.tar.gz"
  "$pkgbase-ffmpeg-$_ffmpeg_version.tar.gz"
  "$pkgbase-fmt-$_fmt_version.tar.gz"
  "$pkgbase-crossguid-$_crossguid_version.tar.gz"
  "$pkgbase-fstrcmp-$_fstrcmp_version.tar.gz"
  "$pkgbase-flatbuffers-$_flatbuffers_version.tar.gz"
)
sha512sums=('2df32e14e1138474cf0a1b8102b4c734e1a54799b1aab049cfe9f623f467e0c9eb87237b4c81ded280e72bc4655a27a887904d164927b3fd227a9c9311531ebc'
            '5185dbdbeb1bd13ea9d8723f1f4ab599d6f3102f5ba1096cd085aa1cda252c045f327c719227bba8e1b742352ade5e335106c8d0c1637a5a6b93ce661620dd7e'
            '11c93eaacd156f8fd7dec7c43d366438b201f31ad55b2870463a9e286912b6ada08882319a021fb7992190f87b909a49f2b83e0321cc17aedc29f7fe5898fa72'
            'b3419ba0a1a2dd70f1bb6236afdfe1c6e88c9ad4264198b289e3bba9375e077cecf7f89848c7b09debaa445327f3507101f3d157e692f7a7163b2bb52643e1e7'
            'a95eaeca26baa9dca4343f1ed6dc068e0800199997a5ad1a28664061e533aa8b0e6d0ad53c18009e21bdd09177b7eda8e59a5a98a10f0f6a081cf03803ee9277'
            'b759a718353254fa8cd981e483bf01a45af0fc76901216404ace5e47f5d3edf43d42422184e5413c221e49832322fdf60d1860e8ec87349c674511064b31e5d6'
            '2682d63609d3dcdfcd8136be632e45df26ad88ce93b9c49745cf728bbd2e6254a7b05c8b059ab581d532372e504206a525a52564b64d076dfdae9c965a09fd16'
            'aaeb0227afd5ada5955cbe6a565254ff88d2028d677d199c00e03b7cb5de1f2c69b18e6e8b032e452350a8eda7081807b01765adbeb8476eaf803d9de6e5509c'
            '0ba07dbe5b2fde1d0a6e14ee26ee2816062541d934eda204b846a30c019362f2626761b628c900293928b9b546dba8ca477c13182e022c3e0e0a142fd67f0696'
            '424dbde693c83d923f82fe22cf42564eb51077bd021fc1cc72d03318fe49d498082494fd57354908a2443aea41f47a280d750d59cee9e78cff4241111a6ceada'
            '539b33f30f6735caaf57fb9f19de449b8a8902362ae9e66a6fceabd530d02888533d2ab262fb187670780c997e5c1d23bd715a3c6860fd50280c1031f47865f7')

prepare() {
  [[ -d kodi-build ]] && rm -rf kodi-build
  mkdir kodi-build

  cd "xbmc-$pkgver-$_codename"

  # detect if building in arch chroot
  if [[ "$srcdir" =~ ^\/build.* ]]; then
    patch -p1 -i "$srcdir/cheat-sse-build.patch"
  fi
}

build() {
  cd kodi-build
  cmake -DCMAKE_INSTALL_PREFIX=/usr \
    -DCMAKE_INSTALL_LIBDIR=/usr/lib \
    -DENABLE_EVENTCLIENTS=ON \
    -DENABLE_INTERNAL_FFMPEG=ON \
    -DENABLE_INTERNAL_FMT=ON \
    -DENABLE_INTERNAL_CROSSGUID=ON \
    -DENABLE_INTERNAL_FSTRCMP=ON \
    -DENABLE_INTERNAL_FLATBUFFERS=ON \
    -Dlibdvdcss_URL="$srcdir/$pkgbase-libdvdcss-$_libdvdcss_version.tar.gz" \
    -Dlibdvdnav_URL="$srcdir/$pkgbase-libdvdnav-$_libdvdnav_version.tar.gz" \
    -Dlibdvdread_URL="$srcdir/$pkgbase-libdvdread-$_libdvdread_version.tar.gz" \
    -DFFMPEG_URL="$srcdir/$pkgbase-ffmpeg-$_ffmpeg_version.tar.gz" \
    -DFMT_URL="$srcdir/$pkgbase-fmt-$_fmt_version.tar.gz" \
    -DCROSSGUID_URL="$srcdir/$pkgbase-crossguid-$_crossguid_version.tar.gz" \
    -DFSTRCMP_URL="$srcdir/$pkgbase-fstrcmp-$_fstrcmp_version.tar.gz" \
    -DFLATBUFFERS_URL="$srcdir/$pkgbase-flatbuffers-$_flatbuffers_version.tar.gz" \
    ../"xbmc-$pkgver-$_codename"
  make 
  make preinstall
}

# kodi
# components: kodi, kodi-bin

package_kodi() {
  pkgdesc="A software media player and entertainment hub for digital media"
  depends=(
    'bluez-libs' 'curl' 'desktop-file-utils' 'freetype2' 'fribidi'
    'hicolor-icon-theme' 'libass' 'libcdio' 'libjpeg-turbo' 'mariadb-libs'
    'libmicrohttpd' 'libpulse' 'libssh' 'libva' 'libvdpau' 'libxrandr'
    'libxslt' 'lzo' 'mesa' 'python2-pillow' 'python2-simplejson' 'smbclient'
    'speex' 'taglib' 'tinyxml' 'xorg-xdpyinfo' 'yajl' 'libbluray'
    'libnfs' 'lirc' 'libcec'
  )
  optdepends=(
    'afpfs-ng: Apple shares support'
    'bluez: Blutooth support'
    'python2-pybluez: Bluetooth support'
    'libnfs: NFS shares support'
    'libplist: AirPlay support'
    'pulseaudio: PulseAudio support'
    'shairplay: AirPlay support'
    'unrar: Archives support'
    'unzip: Archives support'
    'upower: Display battery level'
  )
  provides=('xbmc')
  conflicts=('xbmc')
  replaces=('xbmc')

  _components=(
    'kodi'
    'kodi-bin'
  )

  cd kodi-build
  # install eventclients
  for _cmp in ${_components[@]}; do
  DESTDIR="$pkgdir" /usr/bin/cmake \
    -DCMAKE_INSTALL_COMPONENT="$_cmp" \
     -P cmake_install.cmake
  done

  # python2 is being used
  cd "$pkgdir"
  grep -lR '#!.*python' * | while read file; do sed -s 's/\(#!.*python\)/\12/g' -i "$file"; done
}

# kodi-eventclients
# components: kodi-eventclients-common kodi-eventclients-ps3 kodi-eventclients-wiiremote kodi-eventclients-kodi-send

package_kodi-eventclients() {
  pkgdesc="Kodi Event Clients"
  conflicts=('kodi-eventclients')
  optdepends=('python2: most eventclients are implemented in python2')

  _components=(
    'kodi-eventclients-common'
    'kodi-eventclients-ps3'
    'kodi-eventclients-kodi-send'
  )

  cd kodi-build
  # install eventclients
  for _cmp in ${_components[@]}; do
    DESTDIR="$pkgdir" /usr/bin/cmake \
      -DCMAKE_INSTALL_COMPONENT="$_cmp" \
      -P cmake_install.cmake
  done

  # python2 is being used
  cd "$pkgdir"
  grep -lR '#!.*python' * | while read file; do sed -s 's/\(#!.*python\)/\12/g' -i "$file"; done
}

# kodi-tools-texturepacker
# components: kodi-tools-texturepacker

package_kodi-tools-texturepacker() {
  pkgdesc="Kodi Texturepacker tool"
  depends=('libpng' 'giflib' 'libjpeg-turbo' 'lzo')

  _components=(
    'kodi-tools-texturepacker'
  )

  cd kodi-build
  # install eventclients
  for _cmp in ${_components[@]}; do
    DESTDIR="$pkgdir" /usr/bin/cmake \
      -DCMAKE_INSTALL_COMPONENT="$_cmp" \
      -P cmake_install.cmake
  done
}

# kodi-dev
# components: kodi-addon-dev kodi-audio-dev kodi-eventclients-dev kodi-game-dev kodi-inputstream-dev kodi-peripheral-dev kodi-pvr-dev kodi-screensaver-dev kodi-visualization-dev

package_kodi-dev() {
  pkgdesc="Kodi dev files"
  depends=('kodi')

  _components=(
    'kodi-addon-dev'
    'kodi-audio-dev'
    'kodi-eventclients-dev'
    'kodi-game-dev'
    'kodi-inputstream-dev'
    'kodi-peripheral-dev'
    'kodi-pvr-dev'
    'kodi-screensaver-dev'
    'kodi-visualization-dev'
  )

  cd kodi-build
  # install eventclients
  for _cmp in ${_components[@]}; do
    DESTDIR="$pkgdir" /usr/bin/cmake \
      -DCMAKE_INSTALL_COMPONENT="$_cmp" \
      -P cmake_install.cmake
  done

  # python2 is being used
  cd "$pkgdir"
  grep -lR '#!.*python' * | while read file; do sed -s 's/\(#!.*python\)/\12/g' -i "$file"; done
}
