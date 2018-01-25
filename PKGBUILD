# Maintainer:   Maximilian Weiss <$(echo "bWF4QG1heHdlaXNzLmlv" | base64 -d)>
# Contributor:  Mike Caldwell


pkgname=btcaddress-alpha-bin
pkgver=0.0.1
pkgrel=1


pkgdesc="Casascius Bitcoin Address Utility"

arch=('i686' 'x86_64')

url='https://casascius.wordpress.com/2013/01/26/bitcoin-address-utility/'
#url='https://github.com/casascius/Bitcoin-Address-Utility'

license=('Unknown' 'custom:FOSS')

depends=('mono')

provides=('btcaddress-alpha-bin')
conflicts=('btcaddress-alpha-bin')

source=('btcaddress.png'
        'btcaddress.desktop'
        "btcaddress-alpha.zip::https://ipfs.io/ipfs/QmcbgvdV5qaezKG5tLJ71GXKdikpoH3zHBfNc4SGdbLYN2")
# https://casascius.com/btcaddress-alpha.zip
# HTTPS connection on casascius site is invalid

sha256sums=('3e7e6fcfa81a8617414198c46dfa0fa3489c96ac216e902ec5fabfeb664a9442'
            '1a0321d4e756bbfc06d3b739f64744c0c08f1478a97b27ec92ed342c62da2221'
            '008b92949bbcedebc8da278e2c27156a35b3041e232a4e426efce471a6f2506e')

package() {
    mkdir -p "$pkgdir/opt/btcaddress/"
    mkdir -p "$pkgdir/usr/share/applications/"
    mkdir -p "$pkgdir/usr/share/pixmaps/"
    install -Dm644 "$srcdir/btcaddress.png" "$pkgdir/usr/share/pixmaps/"
    install -Dm644 "$srcdir/btcaddress.desktop" "$pkgdir/usr/share/applications/"
    rm -f "$srcdir/btcaddress.png"
    rm -f "$srcdir/btcaddress.desktop"
    rm -f "$srcdir/btcaddress-alpha.zip"
    rm -f "$srcdir/source.zip"
    cd "$srcdir/"
    for i in *.*; do
        install -Dm644 "$srcdir/$i" "$pkgdir/opt/btcaddress/"
    done
}
