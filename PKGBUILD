# Generated by gem2arch (https://github.com/anatol/gem2arch)
# Maintainer: Anatol Pomozov <anatol.pomozov@gmail.com>

_gemname=actionpack
pkgname=ruby-$_gemname-3
pkgver=3.2.21
pkgrel=1
pkgdesc='Web-flow and rendering framework putting the VC in MVC (part of Rails).'
arch=(any)
url='http://www.rubyonrails.org'
license=(MIT)
depends=(ruby ruby-activesupport-3 ruby-activemodel-3 ruby-rack-cache ruby-builder-3.0 ruby-rack-1.4 ruby-rack-test ruby-journey ruby-sprockets-2.2 ruby-erubis)
options=(!emptydirs)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('1f7ffef317f7808aa3f6b3f63f292c136a827b7c')

package() {
  local _gemdir="$(ruby -e'puts Gem.default_dir')"
  gem install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/MIT-LICENSE" "$pkgdir/usr/share/licenses/$pkgname/MIT-LICENSE"
}
