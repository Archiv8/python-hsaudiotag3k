#!/bin/bash

# Disable various shellcheck rules that produce false positives in this file.
# Repository rules should be added to the .shellcheckrc file located in the
# repository root directory, see https://github.com/koalaman/shellcheck/wiki
# and https://archiv8.github.io for further information.
# shellcheck disable=SC2034,SC2154
# ToDo: Add files: User documentation
# ToDo: Add files: Tooling
# FixMe: Namcap warnings and errors

# Maintainer: Martin Rys <https://rys.pw/#contact_me>
# Previous maintainer: Bijaya Dangol <dangoldbj23@gmail.com>
# Contributor: Ross Clark <archiv8@artisteducator.com>

_reponame=hsaudiotag3k


pkgname=python-hsaudiotag3k
pkgver=1.1.3.post1
pkgrel=3
pkgdesc="Read metadata (tags) of mp3, mp4, wma, ogg, flac and aiff files (python3 version)"
url="https://pypi.org/project/hsaudiotag3k"
arch=(any)
license=("BSD")
depends=(
	"python"
)
makedepends=(
	"python-setuptools"
)
source=("https://pypi.org/packages/source/${_reponame::1}/${_reponame}/${_reponame}-$pkgver.tar.gz")
sha256sums=("ef60e9210d4727e82f0095a686cb07b676d055918f0c59c5bfa8598da03e59d1")

build() {
	cd "$srcdir/${_reponame}-$pkgver"
	python setup.py build
}

package() {
	cd "$srcdir/${_reponame}-$pkgver"
	python setup.py install --root="$pkgdir"
}
