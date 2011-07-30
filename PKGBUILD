# Contributor: Lee.MaRS <leemars@gmail.com>
# Contributor: monson <holymonson@gmail.com>

pkgname=acroread9-fonts
pkgver=9.1.0
pkgrel=3
pkgdesc="Chinese Simplified, Chinese Traditional, Japanese, Korean and Extended Language font packs for Adobe Acrobat Reader 9"
url="http://www.adobe.com/support/downloads/product.jsp?platform=unix&product=10"
license=('custom')
arch=(i686 x86_64)
depends=('acroread>=9.1.0')
source=("http://ardownload.adobe.com/pub/adobe/reader/unix/9.x/9.1/misc/FontPack910_chs_i486-linux.tar.bz2" 
        "http://ardownload.adobe.com/pub/adobe/reader/unix/9.x/9.1/misc/FontPack910_cht_i486-linux.tar.bz2"
        "http://ardownload.adobe.com/pub/adobe/reader/unix/9.x/9.1/misc/FontPack910_jpn_i486-linux.tar.bz2"
        "http://ardownload.adobe.com/pub/adobe/reader/unix/9.x/9.1/misc/FontPack910_kor_i486-linux.tar.bz2"
        "http://ardownload.adobe.com/pub/adobe/reader/unix/9.x/9.1/misc/FontPack910_xtd_i486-linux.tar.bz2")
md5sums=('8abe3f7fb77918a8376b6793b841eaab'
         '38baee4eca2d8291220eb8a8ab77f9b7'
         'b681807c0b8a34c76ec894675d98ec77'
         '76a3dd2511d82c9dc1556bb0f0eae6c1'
         'a2de87858345cf3b2199d4a2fe424b65')

_prefix='/usr/lib/acroread/'

build() {
    cd "$srcdir"
    find $srcdir -name LANG\*.TAR -exec tar -xf {} \;    
    rm Adobe/Reader9/Resource/CMap/Identity-[HV]
}

package() {
    mkdir -p "$pkgdir/$_prefix"    
    mv "$srcdir"/Adobe/Reader9/Resource "$pkgdir/$_prefix"/    
}
