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
pkgname=(
  'kodi' 'kodi-bin' 'kodi-wayland' 'kodi-gbm'
  'kodi-eventclients' 'kodi-tools-texturepacker' 'kodi-dev'
)
pkgver=18.7
pkgrel=0.1
arch=('x86_64')
url="https://kodi.tv"
license=('GPL2')
makedepends=(
  'afpfs-ng' 'bluez-libs' 'cmake' 'curl' 'dav1d' 'doxygen' 'git' 'glew'
  'gperf' 'hicolor-icon-theme' 'java-runtime' 'libaacs' 'libass'
  'libbluray' 'libcdio' 'libcec' 'libgl' 'mariadb-libs' 'libmicrohttpd'
  'libmodplug' 'libmpeg2' 'libnfs' 'libplist' 'libpulse' 'libva'
  'libvdpau' 'libxrandr' 'libxslt' 'lirc' 'lzo' 'mesa' 'nasm'
  'python2-pycryptodomex' 'python2-pillow' 'python2-pybluez'
  'python2-simplejson' 'shairplay' 'smbclient' 'taglib' 'tinyxml' 'swig'
  'upower' 'giflib' 'rapidjson' 'ghostscript' 'meson' 'gtest' 'graphviz'
  # wayland
  'wayland-protocols' 'waylandpp' 'libxkbcommon'
  # gbm
  'libinput'
)

_codename=Leia

_libdvdcss_version="1.4.2-$_codename-Beta-5"
_libdvdnav_version="6.0.0-$_codename-Alpha-3"
_libdvdread_version="6.0.0-$_codename-Alpha-3"
#_ffmpeg_version="4.0.4-$_codename-18.4"
_ffmpeg_version="4.2.2-Matrix-Alpha1"
_fmt_version="6.1.2"
_spdlog_version="1.5.0"
_crossguid_version="8f399e8bd4"
_fstrcmp_version="0.7.D001"
_flatbuffers_version="1.11.0"

source=(
  "$pkgbase-$pkgver-$_codename.tar.gz::https://github.com/xbmc/xbmc/archive/$pkgver-$_codename.tar.gz"
  "$pkgbase-libdvdcss-$_libdvdcss_version.tar.gz::https://github.com/xbmc/libdvdcss/archive/$_libdvdcss_version.tar.gz"
  "$pkgbase-libdvdnav-$_libdvdnav_version.tar.gz::https://github.com/xbmc/libdvdnav/archive/$_libdvdnav_version.tar.gz"
  "$pkgbase-libdvdread-$_libdvdread_version.tar.gz::https://github.com/xbmc/libdvdread/archive/$_libdvdread_version.tar.gz"
  "$pkgbase-ffmpeg-$_ffmpeg_version.tar.gz::https://github.com/xbmc/FFmpeg/archive/$_ffmpeg_version.tar.gz"
  "$pkgbase-fmt-$_fmt_version.tar.gz::http://mirrors.kodi.tv/build-deps/sources/fmt-$_fmt_version.tar.gz"
  "$pkgbase-spdlog-$_spdlog_version.tar.gz::http://mirrors.kodi.tv/build-deps/sources/spdlog-$_spdlog_version.tar.gz"
  "$pkgbase-crossguid-$_crossguid_version.tar.gz::http://mirrors.kodi.tv/build-deps/sources/crossguid-$_crossguid_version.tar.gz"
  "$pkgbase-fstrcmp-$_fstrcmp_version.tar.gz::http://mirrors.kodi.tv/build-deps/sources/fstrcmp-$_fstrcmp_version.tar.gz"
  "$pkgbase-flatbuffers-$_flatbuffers_version.tar.gz::http://mirrors.kodi.tv/build-deps/sources/flatbuffers-$_flatbuffers_version.tar.gz"
  'cheat-sse-build.patch'
  'cpuinfo'
)
noextract=(
  "$pkgbase-libdvdcss-$_libdvdcss_version.tar.gz"
  "$pkgbase-libdvdnav-$_libdvdnav_version.tar.gz"
  "$pkgbase-libdvdread-$_libdvdread_version.tar.gz"
  "$pkgbase-ffmpeg-$_ffmpeg_version.tar.gz"
  "$pkgbase-fmt-$_fmt_version.tar.gz"
  "$pkgbase-spdlog-$_spdlog_version.tar.gz"
  "$pkgbase-crossguid-$_crossguid_version.tar.gz"
  "$pkgbase-fstrcmp-$_fstrcmp_version.tar.gz"
  "$pkgbase-flatbuffers-$_flatbuffers_version.tar.gz"
)
sha512sums=('33f6e1ea948e1ae6efeab23391168b5ea080f3663b653156895b00e48ce33b6b325492e84ad6caf5b46dfb725900520e9a53de17beae919704cc9c424d6203c5'
            '5185dbdbeb1bd13ea9d8723f1f4ab599d6f3102f5ba1096cd085aa1cda252c045f327c719227bba8e1b742352ade5e335106c8d0c1637a5a6b93ce661620dd7e'
            '11c93eaacd156f8fd7dec7c43d366438b201f31ad55b2870463a9e286912b6ada08882319a021fb7992190f87b909a49f2b83e0321cc17aedc29f7fe5898fa72'
            'b3419ba0a1a2dd70f1bb6236afdfe1c6e88c9ad4264198b289e3bba9375e077cecf7f89848c7b09debaa445327f3507101f3d157e692f7a7163b2bb52643e1e7'
            '19bd27687126ffb103a97709dfec7a4330a362410efbbe5ce3a68970d642c1b74c4bc0880600e232b3b34659d7fb0e40e233a8267a9b52921b0f810944a6297a'
            '8770bf4bd2bb6d938e75e0cf1e665c41930dbd9d2a6825274a5a43cd1d85b9c9ca621bb040ed099429f0e16bddbc3399361c453eb1bf3fc01376e6ad9dd875b7'
            '78991c943dd95af563c4b29545b9b5d635caf1af5031262dde734ecf70c0b4ae866d954ee77b050f9f0cc089a3bc57ee9583895e51cb00dd1cc6c10ff905ca34'
            '2682d63609d3dcdfcd8136be632e45df26ad88ce93b9c49745cf728bbd2e6254a7b05c8b059ab581d532372e504206a525a52564b64d076dfdae9c965a09fd16'
            'aaeb0227afd5ada5955cbe6a565254ff88d2028d677d199c00e03b7cb5de1f2c69b18e6e8b032e452350a8eda7081807b01765adbeb8476eaf803d9de6e5509c'
            'e4a6fbc5813041194ac66d2d019aea711dad72239f52731f292675cd21248cba139768aa80f044c3a11cae2d308ae95b4b45de914d207b5b1d3d5d18620c8882'
            '424dbde693c83d923f82fe22cf42564eb51077bd021fc1cc72d03318fe49d498082494fd57354908a2443aea41f47a280d750d59cee9e78cff4241111a6ceada'
            '539b33f30f6735caaf57fb9f19de449b8a8902362ae9e66a6fceabd530d02888533d2ab262fb187670780c997e5c1d23bd715a3c6860fd50280c1031f47865f7')

prepare() {
  # force python 'binary' as python2
  [[ -d "$srcdir/path" ]] && rm -rf "$srcdir/path"
  mkdir "$srcdir/path"
  ln -s /usr/bin/python2 "$srcdir/path/python"

  [[ -d kodi-build-x11 ]] && rm -rf kodi-build-x11
  mkdir kodi-build-x11
  [[ -d kodi-build-wayland ]] && rm -rf kodi-build-wayland
  mkdir kodi-build-wayland
  [[ -d kodi-build-gbm ]] && rm -rf kodi-build-gbm
  mkdir kodi-build-gbm

  cd "xbmc-$pkgver-$_codename"

  # detect if building in arch chroot
  if [[ "$srcdir" =~ ^\/build.* ]]; then
    patch -p1 -i "$srcdir/cheat-sse-build.patch"
  fi
}

build() {
  export PATH="$srcdir/path:$PATH"

  echo "building kodi-x11"
  cd "$srcdir/kodi-build-x11"
  cmake -DCMAKE_INSTALL_PREFIX=/usr \
    -DCMAKE_INSTALL_LIBDIR=/usr/lib \
    -DENABLE_EVENTCLIENTS=ON \
    -DENABLE_INTERNAL_FFMPEG=ON \
    -DENABLE_INTERNAL_FMT=ON \
    -DENABLE_INTERNAL_SPDLOG=ON \
    -DENABLE_INTERNAL_CROSSGUID=ON \
    -DENABLE_INTERNAL_FSTRCMP=ON \
    -DENABLE_INTERNAL_FLATBUFFERS=ON \
    -Dlibdvdcss_URL="$srcdir/$pkgbase-libdvdcss-$_libdvdcss_version.tar.gz" \
    -Dlibdvdnav_URL="$srcdir/$pkgbase-libdvdnav-$_libdvdnav_version.tar.gz" \
    -Dlibdvdread_URL="$srcdir/$pkgbase-libdvdread-$_libdvdread_version.tar.gz" \
    -DFFMPEG_URL="$srcdir/$pkgbase-ffmpeg-$_ffmpeg_version.tar.gz" \
    -DFMT_URL="$srcdir/$pkgbase-fmt-$_fmt_version.tar.gz" \
    -DSPDLOG_URL="$srcdir/$pkgbase-spdlog-$_spdlog_version.tar.gz" \
    -DCROSSGUID_URL="$srcdir/$pkgbase-crossguid-$_crossguid_version.tar.gz" \
    -DFSTRCMP_URL="$srcdir/$pkgbase-fstrcmp-$_fstrcmp_version.tar.gz" \
    -DFLATBUFFERS_URL="$srcdir/$pkgbase-flatbuffers-$_flatbuffers_version.tar.gz" \
    -DX11_RENDER_SYSTEM=gl \
    ../"xbmc-$pkgver-$_codename"
  make
  make preinstall

  echo "building kodi-wayland"
  cd "$srcdir/kodi-build-wayland"
  cmake -DCMAKE_INSTALL_PREFIX=/usr \
    -DCMAKE_INSTALL_LIBDIR=/usr/lib \
    -DENABLE_EVENTCLIENTS=ON \
    -DENABLE_INTERNAL_FFMPEG=ON \
    -DENABLE_INTERNAL_FMT=ON \
    -DENABLE_INTERNAL_SPDLOG=ON \
    -DENABLE_INTERNAL_CROSSGUID=ON \
    -DENABLE_INTERNAL_FSTRCMP=ON \
    -DENABLE_INTERNAL_FLATBUFFERS=ON \
    -Dlibdvdcss_URL="$srcdir/$pkgbase-libdvdcss-$_libdvdcss_version.tar.gz" \
    -Dlibdvdnav_URL="$srcdir/$pkgbase-libdvdnav-$_libdvdnav_version.tar.gz" \
    -Dlibdvdread_URL="$srcdir/$pkgbase-libdvdread-$_libdvdread_version.tar.gz" \
    -DFFMPEG_URL="$srcdir/$pkgbase-ffmpeg-$_ffmpeg_version.tar.gz" \
    -DFMT_URL="$srcdir/$pkgbase-fmt-$_fmt_version.tar.gz" \
    -DSPDLOG_URL="$srcdir/$pkgbase-spdlog-$_spdlog_version.tar.gz" \
    -DCROSSGUID_URL="$srcdir/$pkgbase-crossguid-$_crossguid_version.tar.gz" \
    -DFSTRCMP_URL="$srcdir/$pkgbase-fstrcmp-$_fstrcmp_version.tar.gz" \
    -DFLATBUFFERS_URL="$srcdir/$pkgbase-flatbuffers-$_flatbuffers_version.tar.gz" \
    -DCORE_PLATFORM_NAME=wayland \
    -DWAYLAND_RENDER_SYSTEM=gl \
    ../"xbmc-$pkgver-$_codename"
  make
  make preinstall

  echo "building kodi-gbm"
  cd "$srcdir/kodi-build-gbm"
  cmake -DCMAKE_INSTALL_PREFIX=/usr \
    -DCMAKE_INSTALL_LIBDIR=/usr/lib \
    -DENABLE_EVENTCLIENTS=ON \
    -DENABLE_INTERNAL_FFMPEG=ON \
    -DENABLE_INTERNAL_FMT=ON \
    -DENABLE_INTERNAL_SPDLOG=ON \
    -DENABLE_INTERNAL_CROSSGUID=ON \
    -DENABLE_INTERNAL_FSTRCMP=ON \
    -DENABLE_INTERNAL_FLATBUFFERS=ON \
    -Dlibdvdcss_URL="$srcdir/$pkgbase-libdvdcss-$_libdvdcss_version.tar.gz" \
    -Dlibdvdnav_URL="$srcdir/$pkgbase-libdvdnav-$_libdvdnav_version.tar.gz" \
    -Dlibdvdread_URL="$srcdir/$pkgbase-libdvdread-$_libdvdread_version.tar.gz" \
    -DFFMPEG_URL="$srcdir/$pkgbase-ffmpeg-$_ffmpeg_version.tar.gz" \
    -DFMT_URL="$srcdir/$pkgbase-fmt-$_fmt_version.tar.gz" \
    -DSPDLOG_URL="$srcdir/$pkgbase-spdlog-$_spdlog_version.tar.gz" \
    -DCROSSGUID_URL="$srcdir/$pkgbase-crossguid-$_crossguid_version.tar.gz" \
    -DFSTRCMP_URL="$srcdir/$pkgbase-fstrcmp-$_fstrcmp_version.tar.gz" \
    -DFLATBUFFERS_URL="$srcdir/$pkgbase-flatbuffers-$_flatbuffers_version.tar.gz" \
    -DCORE_PLATFORM_NAME=gbm \
    -DGBM_RENDER_SYSTEM=gles \
    ../"xbmc-$pkgver-$_codename"
  make
  make preinstall
}

# kodi
# components: kodi

package_kodi() {
  pkgdesc="A software media player and entertainment hub for digital media"
  depends=(
    'desktop-file-utils' 'hicolor-icon-theme' 'mesa' 'python2-pycryptodomex'
    'python2-pillow' 'python2-simplejson' 'xorg-xdpyinfo'
    'kodi-bin'
  )
  optdepends=(
    'afpfs-ng: Apple shares support'
    'bluez: Blutooth support'
    'python2-pybluez: Bluetooth support'
    'libplist: AirPlay support'
    'pulseaudio: PulseAudio support'
    'shairplay: AirPlay support'
    'upower: Display battery level'
  )
  provides=('xbmc')
  conflicts=('xbmc')
  replaces=('xbmc')

  _components=(
    'kodi'
    'kodi-bin'
  )

  export PATH="$srcdir/path:$PATH"

  cd kodi-build-x11
  # install eventclients
  for _cmp in ${_components[@]}; do
  DESTDIR="$pkgdir" /usr/bin/cmake \
    -DCMAKE_INSTALL_COMPONENT="$_cmp" \
     -P cmake_install.cmake
  done

  # python2 is being used
  cd "$pkgdir"
  grep -lR '#!.*python' * | \
    while read file; do sed -s 's/\(#!.*python\)/\12/g' -i "$file"; done

  # remove x11 binaries
  rm "$pkgdir/usr/lib/kodi/"{kodi-x11,kodi-xrandr}
}

# kodi-x11
# components: kodi-bin

package_kodi-bin() {
  pkgdesc="x11 kodi binary"
  depends=(
    'bluez-libs' 'curl' 'lcms2' 'libass' 'libbluray' 'libcdio' 'libcec'
    'libmicrohttpd' 'libnfs' 'libpulse' 'libva' 'libvdpau' 'libxrandr'
    'libxslt' 'lirc' 'mariadb-libs' 'python2' 'smbclient' 'taglib'
    'tinyxml' 'kodi'
  )

  cd kodi-build-x11
  install -Dm755 kodi-x11 "$pkgdir/usr/lib/kodi/kodi-x11"
  install -Dm755 kodi-xrandr "$pkgdir/usr/lib/kodi/kodi-xrandr"
}

# kodi-wayland
# components: kodi-bin

package_kodi-wayland() {
  pkgdesc="wayland kodi binary"
  provides=('kodi-bin')
  depends=(
    'bluez-libs' 'curl' 'lcms2' 'libass' 'libbluray' 'libcdio' 'libcec'
    'libmicrohttpd' 'libnfs' 'libpulse' 'libva' 'libxkbcommon' 'libxslt'
    'lirc' 'mariadb-libs' 'python2' 'smbclient' 'taglib' 'tinyxml'
    'waylandpp' 'kodi'
  )

  cd kodi-build-wayland
  install -Dm755 kodi-wayland "$pkgdir/usr/lib/kodi/kodi-wayland"
}

# kodi-gbm
# components: kodi-bin

package_kodi-gbm() {
  pkgdesc="gbm kodi binary"
  provides=('kodi-bin')
  depends=(
    'bluez-libs' 'curl' 'lcms2' 'libass' 'libbluray' 'libcdio' 'libcec'
    'libinput' 'libmicrohttpd' 'libnfs' 'libpulse' 'libva' 'libxkbcommon'
    'libxslt' 'lirc' 'mariadb-libs' 'python2' 'smbclient' 'taglib'
    'tinyxml' 'kodi'
  )

  cd kodi-build-gbm
  install -Dm755 kodi-gbm "$pkgdir/usr/lib/kodi/kodi-gbm"
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

  export PATH="$srcdir/path:$PATH"

  cd kodi-build-x11
  # install eventclients
  for _cmp in ${_components[@]}; do
    DESTDIR="$pkgdir" /usr/bin/cmake \
      -DCMAKE_INSTALL_COMPONENT="$_cmp" \
      -P cmake_install.cmake
  done

  # python2 is being used
  cd "$pkgdir"
  grep -lR '#!.*python' * | \
    while read file; do sed -s 's/\(#!.*python\)/\12/g' -i "$file"; done
}

# kodi-tools-texturepacker
# components: kodi-tools-texturepacker

package_kodi-tools-texturepacker() {
  pkgdesc="Kodi Texturepacker tool"
  depends=('libpng' 'giflib' 'libjpeg-turbo' 'lzo')

  _components=(
    'kodi-tools-texturepacker'
  )

  cd kodi-build-x11
  # install eventclients
  for _cmp in ${_components[@]}; do
    DESTDIR="$pkgdir" /usr/bin/cmake \
      -DCMAKE_INSTALL_COMPONENT="$_cmp" \
      -P cmake_install.cmake
  done
}

# kodi-dev
# components: kodi-addon-dev kodi-audio-dev kodi-eventclients-dev kodi-game-dev
#             kodi-inputstream-dev kodi-peripheral-dev kodi-pvr-dev
#             kodi-screensaver-dev kodi-visualization-dev

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

  export PATH="$srcdir/path:$PATH"

  cd kodi-build-x11
  # install eventclients
  for _cmp in ${_components[@]}; do
    DESTDIR="$pkgdir" /usr/bin/cmake \
      -DCMAKE_INSTALL_COMPONENT="$_cmp" \
      -P cmake_install.cmake
  done

  # python2 is being used
  cd "$pkgdir"
  grep -lR '#!.*python' * | \
    while read file; do sed -s 's/\(#!.*python\)/\12/g' -i "$file"; done
}
