# Contributor: Diego Mascialino <diego@gcoop.coop>
# vim:set ts=2 sw=2 et:
pkgname=ruby-test-unit
_gemname=test-unit
pkgver=2.5.2
pkgrel=1
pkgdesc="Ruby 1.9.x bundles minitest not Test::Unit. Test::Unit bundled in Ruby 1.8.x had not been improved but unbundled Test::Unit (test-unit) is improved actively. "
arch=(any)
url="http://test-unit.rubyforge.org/"
license=('RUBY')      
depends=()
makedepends=('rubygems')
source=("http://rubygems.org/downloads/${_gemname}-${pkgver}.gem")
noextract=("${_gemname}-$pkgver.gem")

build() {
  cd $srcdir
  export HOME=/tmp
  export RHC_RPMBUILD=1
  local _gemdir="$(ruby -rubygems -e'puts Gem.default_dir')"
  gem install --no-user-install --ignore-dependencies -i "${pkgdir}${_gemdir}" -n "${pkgdir}/usr/bin" ${_gemname}-$pkgver.gem
}

md5sums=('29530fd1bb3d53bd6aa20b2c171f516d')


