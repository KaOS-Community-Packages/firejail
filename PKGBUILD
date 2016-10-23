pkgname=firejail
pkgver=0.9.44
pkgrel=1
pkgdesc='Linux namespaces and seccomp-bpf sandbox'
arch=('x86_64')
url='https://firejail.wordpress.com/'
license=(GPL2)
source=(https://github.com/netblue30/firejail/archive/${pkgver}.tar.gz)
md5sums=('f58162fe27f4767ad1e23e90e2c8e6e1')

build(){

    cd "${srcdir}/${pkgname}-${pkgver}"
    ./configure --prefix=/usr
    make

}

package(){

    cd "${srcdir}/${pkgname}-${pkgver}"
    make DESTDIR="${pkgdir}" install
}
