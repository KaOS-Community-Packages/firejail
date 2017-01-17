pkgname=firejail
pkgver=0.9.44.6
pkgrel=1
pkgdesc='Linux namespaces and seccomp-bpf sandbox'
arch=('x86_64')
url='https://firejail.wordpress.com/'
license=(GPL2)
source=(https://github.com/netblue30/firejail/archive/${pkgver}.tar.gz)
md5sums=('62c7eba312875c850a552dd8d4d15583')

build(){

    cd "${srcdir}/${pkgname}-${pkgver}"
    ./configure --prefix=/usr
    make

}

package(){

    cd "${srcdir}/${pkgname}-${pkgver}"
    make DESTDIR="${pkgdir}" install
}
