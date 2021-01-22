pkgname=firejail
pkgver=0.9.64
pkgrel=1
pkgdesc='Linux namespaces and seccomp-bpf sandbox'
arch=('x86_64')
url='https://firejail.wordpress.com/'
license=(GPL2)
source=("https://github.com/netblue30/firejail/archive/${pkgver}.tar.gz")
md5sums=('7d5fd670a5043ee387a33119aa6704dc')

build(){

    cd "${srcdir}/${pkgname}-${pkgver}"
    ./configure --prefix=/usr
    make -j$(nproc)

}

package(){

    cd "${srcdir}/${pkgname}-${pkgver}"
    make DESTDIR="${pkgdir}" install
}
