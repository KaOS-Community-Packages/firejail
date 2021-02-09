pkgname=firejail
pkgver=0.9.64.4
pkgrel=1
pkgdesc='Linux namespaces and seccomp-bpf sandbox'
arch=('x86_64')
url='https://firejail.wordpress.com/'
license=(GPL2)
source=("https://github.com/netblue30/firejail/archive/${pkgver}.tar.gz")
md5sums=('e5e797eb466f2bb5d3f5bdb2dba32d77')

build(){

    cd "${srcdir}/${pkgname}-${pkgver}"
    ./configure --prefix=/usr
    make -j$(nproc)

}

package(){

    cd "${srcdir}/${pkgname}-${pkgver}"
    make DESTDIR="${pkgdir}" install
}
