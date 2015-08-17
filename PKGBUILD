# Maintainer: Thorsten Töpper <atsutane-aur@freethoughts.de>

pkgname=structorizer
pkgver=3.22
_pkgver=3_22
pkgrel=1
pkgdesc="A little tool which you can use to create Nassi-Schneiderman Diagrams (NSD)"
arch=('any')
url="http://structorizer.fisch.lu/"
license=('custom')
depends=('java-runtime' 'sh')
install="structorizer.install"
source=("${pkgname}-${pkgver}.zip::http://www.fisch.lu/Php/download.php?file=${pkgname}_${_pkgver}.zip")
md5sums=('c72a31a57d44e4c26b0bdca4cfea5c0d')

build() {
  echo -n '#!/bin/sh
cd /usr/share/java/structorizer || return 1
java -jar Structorizer.jar Structorizer' > ${srcdir}/structorizer
}

package() {
  # Binaries
  install -Dm755 \
    ${srcdir}/Structorizer/Structorizer.app/Contents/Resources/Java/Structorizer.jar \
    ${pkgdir}/usr/share/java/${pkgname}/Structorizer.jar
  install -Dm755 \
    ${srcdir}/Structorizer/Structorizer.app/Contents/Resources/Java/lib/AppleJavaExtensions.jar \
    ${pkgdir}/usr/share/java/${pkgname}/lib/AppleJavaExtensions.jar
  install -Dm755 \
    ${srcdir}/Structorizer/Structorizer.app/Contents/Resources/Java/lib/bsh-2.0b4.jar \
    ${pkgdir}/usr/share/java/${pkgname}/lib/bsh-2.0b4.jar
  install -Dm755 \
    ${srcdir}/Structorizer/Structorizer.app/Contents/Resources/Java/lib/freehep-graphics2d-2.1.1.jar \
    ${pkgdir}/usr/share/java/${pkgname}/lib/freehep-graphics2d-2.1.1.jar
  install -Dm755 \
    ${srcdir}/Structorizer/Structorizer.app/Contents/Resources/Java/lib/freehep-graphicsio-2.1.1.jar \
    ${pkgdir}/usr/share/java/${pkgname}/lib/freehep-graphicsio-2.1.1.jar
  install -Dm755 \
    ${srcdir}/Structorizer/Structorizer.app/Contents/Resources/Java/lib/freehep-io-2.0.2.jar \
    ${pkgdir}/usr/share/java/${pkgname}/lib/freehep-io-2.0.2.jar
  install -Dm755 \
    ${srcdir}/Structorizer/Structorizer.app/Contents/Resources/Java/lib/freehep-graphicsio-svg-2.1.1.jar \
    ${pkgdir}/usr/share/java/${pkgname}/lib/freehep-graphicsio-svg-2.1.1.jar
  install -Dm755 \
    ${srcdir}/Structorizer/Structorizer.app/Contents/Resources/Java/lib/freehep-swing-2.0.3.jar \
    ${pkgdir}/usr/share/java/${pkgname}/lib/freehep-swing-2.0.3.jar
  install -Dm755 \
    ${srcdir}/Structorizer/Structorizer.app/Contents/Resources/Java/lib/freehep-util-2.0.2.jar \
    ${pkgdir}/usr/share/java/${pkgname}/lib/freehep-util-2.0.2.jar
  install -Dm755 \
    ${srcdir}/Structorizer/Structorizer.app/Contents/Resources/Java/lib/freehep.jar \
    ${pkgdir}/usr/share/java/${pkgname}/lib/freehep.jar
  install -Dm755 \
    ${srcdir}/Structorizer/Structorizer.app/Contents/Resources/Java/lib/swing-layout-1.0.3.jar \
    ${pkgdir}/usr/share/java/${pkgname}/lib/swing-layout-1.0.3.jar
  
  # Script and license
  install -Dm755 \
    ${srcdir}/structorizer \
    ${pkgdir}/usr/bin/structorizer
  install -Dm 644 \
    ${srcdir}/Structorizer/license.txt \
    ${pkgdir}/usr/share/licenses/${pkgname}/LICENSE
}

# vim:set ts=2 sw=2 et:

