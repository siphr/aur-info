# Maintainer: siphr <archlinux@techtum.dev>
pkgname=aur-info
pkgver=0.3
pkgrel=1
pkgdesc="Retrieve package info for an aur package."
depends=(python)
arch=(x86_64)
source=("https://github.com/siphr/aur-info.git")
license=('MIT')
install=.install

build() {
    echo "echo `date`" > aur-info
    echo "python -m aur_info \$@" >> aur-info

    chmod +x $srcdir/aur-info
}

package() {
    mkdir -p $pkgdir/usr/bin
#    echo $srcdir
    cp "$srcdir/aur-info" "$pkgdir/usr/bin/aur-info"
    echo 'Finsihed setting up aur-info.'
}
