<p align="center">
  <img src="./logo.svg" width="250" alt="Mersel" />
</p>

<h1 align="center">Open Source</h1>

<p align="center">
  Türkiye e-Dönüşüm ekosistemi için açık kaynak mikroservisler geliştiriyoruz.
</p>

<p align="center">
  <a href="https://mersel.io">mersel.io</a>
</p>

---

## Hakkımızda

**Mersel**, Türkiye'deki e-Fatura, e-İrsaliye, e-Arşiv, e-Defter ve diğer e-Dönüşüm süreçleri için altyapı yazılımları geliştiren bir teknoloji şirketidir. Bu organizasyon altında, e-Dönüşüm ve yan dikeylerde kullandığımız temel servis bileşenlerini açık kaynak olarak yayınlıyoruz.

Amacımız, Türkiye'deki yazılım ekosisteminde e-Dönüşüm entegrasyonunu kolaylaştırmak ve topluluğa katkı sağlamaktır.

## Açık Kaynak Projelerimiz

### 🔄 [ebelge-xslt-service](https://github.com/mersel-os/ebelge-xslt-service)

XML Schema/Schematron doğrulama ve XSLT dönüşüm mikroservisi.

- **GİB UBL-TR** belge doğrulama (XSD + Schematron) — e-Fatura, e-İrsaliye, e-Arşiv, e-Defter
- **XSLT dönüşüm** — XML belgelerden HTML görüntüleme (gömülü XSLT desteği)
- **Doğrulama profilleri** — İmzasız belge doğrulama, kural bastırma
- **GİB paket otomatik sync** — Resmi GİB paketlerini API ile indir ve güncelle
- **Hot-reload** — Dosya değişikliğinde veya API ile restart gerektirmeden yeniden yükleme
- **Web arayüzü** — React + TailwindCSS + shadcn/ui ile doğrulama ve dönüşüm arayüzü

> Java 21 · Spring Boot 3.4 · Saxon HE · Docker · Prometheus + Grafana

---

### 📄 [html-to-pdf](https://github.com/mersel-os/html-to-pdf)

Playwright (Chromium) ve PdfSharpCore ile geliştirilmiş, hafif ve yüksek kaliteli HTML → PDF dönüşüm mikroservisi.

- **Tekli ve çoklu HTML → PDF** dönüşümü (birleştirme desteği)
- **wkhtmltopdf uyumlu** preset'ler ile kolay geçiş
- **İstemci SDK** — .NET için hazır NuGet paketi ([`MERSEL.Services.HtmlToPdf.Client`](https://www.nuget.org/packages/MERSEL.Services.HtmlToPdf.Client))
- **Yatay ölçeklenebilir** — Stateless mimari, load balancer arkasında çalışır
- **Observability** — OpenTelemetry + Prometheus metrikleri, hazır Grafana dashboard

> .NET 9 · Playwright · Minimal API · Docker · NuGet

---

### 👥 [gib-user-list](https://github.com/mersel-os/gib-user-list)

GİB e-Fatura ve e-İrsaliye mükellef listelerini senkronize eden ve sorgulatan mikroservis.

- **~200 MB RAM ile tam senkronizasyon** — Stream tabanlı XML parsing, milyonlarca kaydı düşük bellek kullanımıyla işler
- **Sıfır kesinti güncelleme** — PostgreSQL Materialized View ile güncelleme sırasında API kesintiye uğramaz
- **Veritabanı bağımsız** — Kendi uygulamalarınız hangi DB'yi kullanırsa kullansın, HTTP API ile entegre olur
- **Delta sync desteği** — `/changes` endpoint'i ile sadece değişiklikleri takip edin
- **İstemci SDK** — .NET için hazır NuGet paketi ([`MERSEL.Services.GibUserList.Client`](https://www.nuget.org/packages/MERSEL.Services.GibUserList.Client))
- **HMAC kimlik doğrulama** — Internal servis güvenliği için opsiyonel HMAC-SHA256
- **Webhook bildirimleri** — Slack ve HTTP webhook desteği ile sync durumu takibi
- **Observability** — OpenTelemetry + Prometheus metrikleri, hazır Grafana dashboard

> .NET 9 · PostgreSQL · EF Core 9 · Minimal API · Docker · Kubernetes · NuGet

---

## Kullanım Alanları

Bu servisler, e-Dönüşüm yazılımlarında yaygın olarak ihtiyaç duyulan bileşenlerdir:

| İhtiyaç | Servis |
|---------|--------|
| GİB'e göndermeden önce belge doğrulama | [ebelge-xslt-service](https://github.com/mersel-os/ebelge-xslt-service) |
| e-Fatura/e-İrsaliye XML → HTML görüntüleme | [ebelge-xslt-service](https://github.com/mersel-os/ebelge-xslt-service) |
| HTML fatura/rapor → PDF dönüştürme | [html-to-pdf](https://github.com/mersel-os/html-to-pdf) |
| wkhtmltopdf'den modern altyapıya geçiş | [html-to-pdf](https://github.com/mersel-os/html-to-pdf) |
| e-Fatura/e-İrsaliye mükellef sorgulama | [gib-user-list](https://github.com/mersel-os/gib-user-list) |
| GİB mükellef listesi senkronizasyonu | [gib-user-list](https://github.com/mersel-os/gib-user-list) |
| VKN/TCKN ile mükellef doğrulama | [gib-user-list](https://github.com/mersel-os/gib-user-list) |

## Katkıda Bulunma

Tüm projelerimiz MIT lisansı ile yayınlanmaktadır. Katkılarınızı bekliyoruz — her repo kendi `CONTRIBUTING` rehberini içerir.

1. İlgili repoyu fork edin
2. Feature branch oluşturun
3. Pull Request açın

Sorularınız veya önerileriniz için [Issues](https://github.com/orgs/mersel-os/repositories) bölümünü kullanabilirsiniz.

---

<p align="center">
  <sub>Mersel tarafından özenle geliştirilmektedir.</sub>
</p>
