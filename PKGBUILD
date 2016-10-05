pkgname=firejail
pkgver=0.9.42
pkgrel=1
pkgdesc='Linux namespaces and seccomp-bpf sandbox'
arch=('x86_64')
url='https://firejail.wordpress.com/'
license=(GPL2)
source=(https://github.com/netblue30/firejail/archive/${pkgver}.tar.gz)
md5sums=('b6d2e6d5fcecabee92cc3957d5b8cb4f')

build(){

    cd "${srcdir}/${pkgname}-${pkgver}"
    ./configure --prefix=/usr
    make

}

package(){

    cd "${srcdir}/${pkgname}-${pkgver}"
    make DESTDIR="${pkgdir}" install
}
