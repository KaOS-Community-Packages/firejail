pkgname=firejail
pkgver=0.9.44.8
pkgrel=1
pkgdesc='Linux namespaces and seccomp-bpf sandbox'
arch=('x86_64')
url='https://firejail.wordpress.com/'
license=(GPL2)
source=(https://github.com/netblue30/firejail/archive/${pkgver}.tar.gz)
md5sums=('95eec0a2d212b6a3631042aff04a2c3e')

build(){

    cd "${srcdir}/${pkgname}-${pkgver}"
    ./configure --prefix=/usr
    make

}

package(){

    cd "${srcdir}/${pkgname}-${pkgver}"
    make DESTDIR="${pkgdir}" install
}
