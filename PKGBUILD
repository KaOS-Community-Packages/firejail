pkgname=firejail
pkgver=0.9.64.2
pkgrel=1
pkgdesc='Linux namespaces and seccomp-bpf sandbox'
arch=('x86_64')
url='https://firejail.wordpress.com/'
license=(GPL2)
source=("https://github.com/netblue30/firejail/archive/${pkgver}.tar.gz")
md5sums=('cd62ff0b5c3afc99fb9ed50ced1686f9')

build(){

    cd "${srcdir}/${pkgname}-${pkgver}"
    ./configure --prefix=/usr
    make -j$(nproc)

}

package(){

    cd "${srcdir}/${pkgname}-${pkgver}"
    make DESTDIR="${pkgdir}" install
}
