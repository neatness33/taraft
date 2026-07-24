# Taraftarium24

Bağımsız spor bilgi ve **yasal maç yayın rehberi** sitesi.

**Domain:** https://taraftarium24.store  
**Teknoloji:** Saf HTML / CSS / JS (Node.js yok, build yok)  
**Barındırma:** GitHub Pages + özel domain

## Yasal not

Bu site:

- canlı maç yayını barındırmaz
- IPTV aboneliği satmaz / önermez
- APK dosyası dağıtmaz
- yayın haklarına sahip değildir
- yalnızca spor bilgisi, fikstür ve yasal yayıncı bilgilendirmesi sunar

## Klasör yapısı

```
/
├── index.html
├── 404.html
├── CNAME
├── robots.txt
├── sitemap.xml
├── rss.xml
├── manifest.webmanifest
├── humans.txt
├── .well-known/security.txt
├── assets/css/style.css
├── assets/js/config.js
├── assets/js/main.js
└── [sayfa-adi]/index.html
```

## GitHub’a yükleme

1. Yeni bir GitHub deposu oluşturun.
2. Bu klasörün tüm içeriğini yükleyin (`git push` veya GitHub web arayüzü).
3. **Settings → Pages**:
   - Source: **GitHub Actions** (önerilen) veya `main` branch / root
4. Özel domain olarak `taraftarium24.store` ekleyin.
5. DNS’te:
   - `A` kayıtları GitHub Pages IP’lerine
   - veya `CNAME` → `kullanici.github.io`
6. HTTPS’i etkinleştirin.

`CNAME` dosyası zaten `taraftarium24.store` içerir.

## Analitik / sohbet ayarı

Tüm kimlikler tek dosyada:

`assets/js/config.js`

- `ga4MeasurementId` → Google Analytics 4
- `gscVerification` → Search Console meta doğrulama
- `clarityProjectId` → Microsoft Clarity
- `tawkTo` → Tawk.to (şu an verdiğiniz kimliklerle etkin)

## Yerel önizleme

Herhangi bir statik sunucu yeterli. Örnek (Python):

```bash
python -m http.server 8080
```

Tarayıcıda: http://localhost:8080
