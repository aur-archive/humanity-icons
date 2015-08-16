# Contributor: pumbur <free@pumbur.net>
# Contributor: jib <jbc.as (AT) free.fr>
# Contributer: giacomogiorgianni@gmail.com

pkgname=humanity-icons
_pkgname=humanity-icon-theme
pkgver=0.6.5
pkgrel=1
pkgdesc="Humanity icons from Ubuntu + Arch main menu icon"
url="https://launchpad.net/humanity"
arch=(any)
license=(GPL2)
depends=('gtk2')
install='humanity.install'
conflicts=('humanity-icon-theme')
source=(https://launchpad.net/ubuntu/+archive/primary/+files/${_pkgname}_${pkgver}.tar.gz
        {16,22,24,32,48,64}.svg)

package(){
  cd ${srcdir}/${_pkgname}-${pkgver}
  mkdir -p $pkgdir/usr/share/icons
  cp -r ./Human*/ $pkgdir/usr/share/icons
  rm $pkgdir/usr/share/icons/Humanity{,-Dark}/COPYING
  cd  $pkgdir/usr/share/icons
  rm ./Humanity{,-Dark}/places/*/{start-here,distributor-logo}.svg
  for _r in {16,22,24,32,48,64}; do
    for _d in {"Humanity","Humanity-Dark"}; do
      cd $pkgdir/usr/share/icons/$_d/places/$_r
      cp $srcdir/$_r.svg ./start-here.svg
      ln -s start-here.svg distributor-logo.svg
    done
  done
}

md5sums=('dd68fd7f3ea831182d042a7ee75e50bc'
         '123d1c18b3843056b496918f5dbd392d'
         '60c66e017acf488cfe9455e1c6d105f9'
         '7ad714ee2dc7373766d0ea6c90f53f20'
         'dbcdfd5ef777c97bb0e27b5a18709fff'
         'bac45253bc7b32884cf79308bf07ff70'
         'fe72f0780a2691b67f3a2d9cb5965ba0')
