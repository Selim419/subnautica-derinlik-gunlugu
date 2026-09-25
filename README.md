# subnautica-derinlik-gunlugu

Bu depo build çıktısı **tutmaz**. Alt yol site, içeriği
[`Selim419/subnautica-source`](https://github.com/Selim419/subnautica-source)
reposundan GitHub Actions ile yayınlar.

- Kaynak: <https://github.com/Selim419/subnautica-source>
- Canlı: <https://selim419.github.io/subnautica-derinlik-gunlugu/>

## Bu depoda ne var

| Dosya | Rol |
| --- | --- |
| `.github/workflows/deploy.yml` | `main` push'una tepki verir, `.deploy-source`'ta adı geçen commit'i derler ve yayınlar |
| `.deploy-source` | Bu deponun yayınlayacağı **kaynak** commit SHA'sı |

Bu iş akışı kök siteyle (`Selim419/Selim419.github.io`) neredeyse aynıdır; tek fark
`npm run build:subpath` kullanması ve taban yolunu
`/subnautica-derinlik-gunlugu/` olarak doğrulamasıdır. İki dosya arasında tam olarak
dört satır fark vardır ve bu, kazara yer değiştirmeyi yakalamak için test edilir.

## Neden iki ayrı Pages deposu

Kök site `Selim419/Selim419.github.io` üzerinden sunulur. GitHub bir kullanıcı
sayfası deposundan yalnızca bir site yayınlayabildiği için alt yol ayrı bir depo
ister — ve taban yolu farklı olduğu için ayrı bir derleme gerektirir.

Bu pipeline'da secret, token veya API anahtarı yoktur.
