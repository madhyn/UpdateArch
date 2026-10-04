# Maintainer: madhyn <https://github.com/madhyn>
pkgname=updatearch
pkgver=1.0.0
pkgrel=1
pkgdesc="Autonomous System Tray & Update Guard for Arch Linux with native Wayland/SNI integration"
arch=('any')
url="https://github.com/madhyn/UpdateArch"
license=('MIT')
depends=(
    'python'
    'python-pyqt6'
    'pacman-contrib'
)
optdepends=(
    'yay: Support for Arch User Repository (AUR) packages'
    'needrestart: Kernel, microcode and shared library restart diagnostics'
    'rkhunter: Security audit and tool definition updates'
)
source=("$pkgname-$pkgver.tar.gz::$url/archive/refs/tags/v$pkgver.tar.gz")
sha256sums=('2822ba361353a2e3b4f4a5feffc5a7762f7d86b02b87001fb36dcc3f5b96fe5f')

package() {
    cd "$srcdir/UpdateArch-$pkgver" 2>/dev/null || cd "$startdir"

    install -Dm755 updatearch "$pkgdir/usr/bin/updatearch"
    install -Dm644 updatearch.desktop "$pkgdir/usr/share/applications/updatearch.desktop"
    install -Dm644 updatearch-autostart.desktop "$pkgdir/etc/xdg/autostart/updatearch.desktop"
    install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
    install -Dm644 README.md "$pkgdir/usr/share/doc/$pkgname/README.md"
}
