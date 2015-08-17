# Contributor: Xavion <Xavion (dot) 0 (at) Gmail (dot) com>
# Contributor: Bruenig <Matthew (dot) Bruenig (at) Gmail (dot) com>

pkgname=pacwrap
pkgver=0.2.2
pkgrel=1
pkgdesc="Wraps the 'pacman' and 'packer' tools - replaced by the 'packer-color' package"
arch=("any")
url="https://github.com/bruenig/pacwrap"
license=("GPL3")
depends=("bash" "packer")
options=(!emptydirs)
source=(${pkgname})

package() {
	cd "${srcdir}"

	# Messages
	warning "Due to coding changes in 'packer', install the 'packer-color' package instead."
	read -p "Are you sure that you want to continue building this package despite its deprecated status? [y/N] " -n 1
	if [[ ! $REPLY =~ ^[Yy]$ ]]; then
		echo ""
		return 1
	fi

	install -D -m755 ${pkgname} "${pkgdir}"/usr/bin/${pkgname}
}

sha1sums=('200d9c797d877ca5db69177d7610ba198d452bcc')
