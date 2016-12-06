pkgname=firejail
pkgver=0.9.44.2
pkgrel=1
pkgdesc='Linux namespaces and seccomp-bpf sandbox'
arch=('x86_64')
url='https://firejail.wordpress.com/'
license=(GPL2)
source=(https://github.com/netblue30/firejail/archive/${pkgver}.tar.gz)
md5sums=('52e296946129e430092fb0dce1ecb3a3')

build(){

    cd "${srcdir}/${pkgname}-${pkgver}"
    ./configure --prefix=/usr
    make

}

package(){

    cd "${srcdir}/${pkgname}-${pkgver}"
    make DESTDIR="${pkgdir}" install
}
