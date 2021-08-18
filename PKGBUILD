# Maintainer: Mesmer <mesmer@fisica.if.uff.br>
pkgname=duckdns
pkgver=1.0
pkgrel=1
pkgdesc="Update your DuckDNS.org entries from your computer without setting up any cronjob. You just need to create config files for your domains."
arch=("any")
install="duckdns.install"
url="https://www.duckdns.org"
backup=("etc/duckdns.d/default.cfg")

source=("duckdns" "default.cfg" "duckdns.service" "duckdns.timer")

md5sums=("c668ea8f621bca94cb5a39034b5ae7ea"
         "4cad7ae6c25b8148916fc702f4846a6f"
         "1b121d4e8671a251e3bfd1509c39ba57"
         "2a546e67b9627b7c64cafef05120d074")


package() {

    install -Dm0755 duckdns         "${pkgdir}/usr/bin/duckdns"

    install -dm0700                 "${pkgdir}/etc/duckdns.d/"
    install -Dm0600 default.cfg     "${pkgdir}/etc/duckdns.d/default.cfg"

    install -Dm0644 duckdns.service "${pkgdir}/usr/lib/systemd/system/duckdns.service"
    install -Dm0644 duckdns.timer   "${pkgdir}/usr/lib/systemd/system/duckdns.timer"
}
