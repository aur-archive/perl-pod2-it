# Mantainer: Simone Sclavi 'Ito' <darkhado@gmail.com>
pkgname=perl-pod2-it
pkgver=0.18
pkgrel=1
_realname=POD2-IT
pkgdesc='Italian Translation of Perl Documentation'
arch=('any')
url='http://pod2it.sourceforge.net'
license=('GPL' 'PerlArtistic')
depends=('perl')
options=(!emptydirs !purge)
source=(http://netcologne.dl.sourceforge.net/project/pod2it/pod2it/$_realname-$pkgver.tar.gz)
md5sums=('64da8a6c5414af07d33c59cec1110d13')

build(){
    chmod -R 755 $_realname-$pkgver
    cd $_realname-$pkgver
    perl Makefile.PL INSTALLDIRS=vendor 
    make
}
check(){
    cd $_realname-$pkgver
    make test
}
package(){
    cd $_realname-$pkgver
    make install DESTDIR=$pkgdir 
    find ${pkgdir} -name perllocal.pod -delete
    find ${pkgdir} -name .packlist -delete
}
