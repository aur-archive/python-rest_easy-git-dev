# Maintainer: David McInnis <davidm at eagles dot ewu dot edu>

pkgname=python-rest_easy-git-dev
_gitname=('rest_easy')
pkgver=38bd80f
pkgrel=3
pkgdesc="Dynamically creates wrappers for RESTful APIs from YAML markup"
url="https://github.com/reklaklislaw/${_gitname}"
arch=('any')
license=('GPL')
depends=('python-lxml' 'python-yaml' 'python-xmltodict' 'python-dicttoxml')
makedepends=('python-setuptools')
source=("git+https://github.com/reklaklislaw/${_gitname}.git")
sha256sums=('SKIP')

pkgver() {
  cd $srcdir/$_gitname
  git log -1 --format="%h" --date=short
}


package () {
  pkgdesc+=" (Python3.x)"

  cd $srcdir/$_gitname
  python setup.py install --root="${pkgdir}" --optimize=1
  
  install -D README.md $pkgdir/usr/share/doc/$pkgname/README.md
}
