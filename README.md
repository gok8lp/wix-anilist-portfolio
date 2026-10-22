# Wix AniList Portfolio

Wix Velo üzerinde kişisel site ve AniList verisi gösterme denemesi.
Page-code experiments for a Wix portfolio with AniList integration.

Bu depo **tam bir statik web sitesi dışa aktarımı değildir**. Sayfa tasarımları ve Wix editöründeki öğeler
Wix tarafında bulunur; yalnızca bu dosyaları açmak siteyi çalıştırmaz.

## İçerik

| Yol | Görev |
| --- | --- |
| `src/pages/masterPage.js` | AniList GraphQL sorgusu ve ortak sayfa denemesi |
| `src/pages/Hobies.ch7ux.js` | Hobi sayfasındaki AniList denemesi |
| `src/pages/*.js` | Diğer sayfaların Velo kodları ve başlangıç şablonları |
| `src/backend/` | Wix arka uç izinleri |
| `wix.config.json` | Bağlı Wix projesi yapılandırması |

## Geliştirme

Bağlı Wix sitesine erişim, Node.js ve projenin desteklediği Wix CLI gerekir.
`package.json` içindeki `dev` ve `lint` komutları kullanılır. Bağımlılık kurulumu `wix sync-types`
çağıran bir postinstall işlemi içerir ve Wix hesabına/siteye erişim gerektirebilir.

```bash
npm install
npm run dev
```

Bu komutlar site erişimi olan geliştirme ortamı içindir; GitHub Pages üzerinde çalışmaz.

## Mevcut durum

Öğrenme prototipidir. Bazı sayfalar başlangıç şablonudur; hobi sayfasında import satırı callback içine
konulduğundan düzeltilmeden standart JavaScript olarak ayrıştırılamaz. Site çalışır/dağıtıma hazır diye sunulmaz.
AniList kullanıcı adını, sorgu alanlarını ve Wix öğe kimliklerini kendi sayfana göre uyarlamalısın.
Kişisel statik site ayrı depodadır: [gok8lp.github.io](https://github.com/gok8lp/gok8lp.github.io).
