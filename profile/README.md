<div align="center">

<br/>

# mersel open source

**Türkiye e-Dönüşüm ekosistemi için production-ready mikroservisler**

e-Fatura · e-İrsaliye · e-Arşiv · e-Defter · e-İmza

<br/>

[![Website](https://img.shields.io/badge/mersel.io-0a0a0a?style=for-the-badge&logo=safari&logoColor=white)](https://mersel.io)
&nbsp;&nbsp;
[![License](https://img.shields.io/badge/MIT-green?style=for-the-badge&label=license)](https://opensource.org/licenses/MIT)
&nbsp;&nbsp;
[![GitHub](https://img.shields.io/badge/mersel--os-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/mersel-os)

<br/>

</div>

> Mersel, Türkiye'deki e-Dönüşüm süreçleri için altyapı yazılımları geliştiren bir teknoloji şirketidir.
> Bu organizasyon altında, e-Dönüşüm ve yan dikeylerde kullandığımız temel servis bileşenlerini açık kaynak olarak yayınlıyoruz.

<br/>

## Projeler

<table>
<tr>
<td>

### [`ebelge-xslt-service`](https://github.com/mersel-os/ebelge-xslt-service)

XML Schema / Schematron doğrulama ve XSLT dönüşüm mikroservisi.

GİB UBL-TR belge doğrulama, XML → HTML dönüşüm, otomatik GİB paket senkronizasyonu, hot-reload ve React tabanlı web arayüzü.

![Java](https://img.shields.io/badge/Java_21-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot_3.4-6DB33F?style=flat-square&logo=spring-boot&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)

[![Stars](https://img.shields.io/github/stars/mersel-os/ebelge-xslt-service?style=flat-square&label=stars&color=yellow)](https://github.com/mersel-os/ebelge-xslt-service)

</td>
</tr>
<tr>
<td>

### [`html-to-pdf`](https://github.com/mersel-os/html-to-pdf)

Playwright (Chromium) tabanlı, yüksek kaliteli HTML → PDF dönüşüm mikroservisi.

Tekli/çoklu dönüşüm, wkhtmltopdf uyumlu preset'ler, .NET istemci SDK'sı, stateless mimari ve OpenTelemetry observability.

![.NET 9](https://img.shields.io/badge/.NET_9-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![NuGet](https://img.shields.io/badge/NuGet-004880?style=flat-square&logo=nuget&logoColor=white)

[![Stars](https://img.shields.io/github/stars/mersel-os/html-to-pdf?style=flat-square&label=stars&color=yellow)](https://github.com/mersel-os/html-to-pdf)

</td>
</tr>
<tr>
<td>

### [`gib-user-list`](https://github.com/mersel-os/gib-user-list)

GİB e-Fatura ve e-İrsaliye mükellef listelerini senkronize eden ve sorgulatan mikroservis.

~200 MB RAM ile milyon kayıt, sıfır kesintili güncelleme, delta sync, HMAC auth, webhook bildirimleri ve .NET istemci SDK'sı.

![.NET 9](https://img.shields.io/badge/.NET_9-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)

[![Stars](https://img.shields.io/github/stars/mersel-os/gib-user-list?style=flat-square&label=stars&color=yellow)](https://github.com/mersel-os/gib-user-list)

</td>
</tr>
<tr>
<td>

### [`sign-api`](https://github.com/mersel-dss/mersel-dss-server-signer-java) <sup>`mersel-dss`</sup>

Türkiye e-imza standartlarına uygun elektronik imza (XAdES, PAdES, WS-Security) servisi.

e-Fatura / e-Arşiv XML imzalama, PDF dijital imzalama, SOAP imzalama, HSM/PKCS#11 desteği, KamuSM root sertifika yönetimi ve RFC 3161 zaman damgası.

![Java](https://img.shields.io/badge/Java_8+-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=spring-boot&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)

[![Stars](https://img.shields.io/github/stars/mersel-dss/mersel-dss-server-signer-java?style=flat-square&label=stars&color=yellow)](https://github.com/mersel-dss/mersel-dss-server-signer-java)
[![Docs](https://img.shields.io/badge/docs-dss.mersel.dev-blue?style=flat-square)](https://dss.mersel.dev)

</td>
</tr>
</table>

<br/>

## Ne Zaman Kullanmalı?

| Senaryo | Servis |
|:--------|:------:|
| GİB'e göndermeden önce belge doğrulama | [`ebelge-xslt-service`](https://github.com/mersel-os/ebelge-xslt-service) |
| e-Fatura / e-İrsaliye XML → HTML görüntüleme | [`ebelge-xslt-service`](https://github.com/mersel-os/ebelge-xslt-service) |
| HTML fatura / rapor → PDF dönüştürme | [`html-to-pdf`](https://github.com/mersel-os/html-to-pdf) |
| wkhtmltopdf'den modern altyapıya geçiş | [`html-to-pdf`](https://github.com/mersel-os/html-to-pdf) |
| e-Fatura / e-İrsaliye mükellef sorgulama | [`gib-user-list`](https://github.com/mersel-os/gib-user-list) |
| VKN / TCKN ile mükellef doğrulama | [`gib-user-list`](https://github.com/mersel-os/gib-user-list) |
| e-Fatura / e-Arşiv XML imzalama (XAdES) | [`sign-api`](https://github.com/mersel-dss/mersel-dss-server-signer-java) |
| PDF dijital imzalama (PAdES) | [`sign-api`](https://github.com/mersel-dss/mersel-dss-server-signer-java) |
| HSM / PKCS#11 ile donanımsal imzalama | [`sign-api`](https://github.com/mersel-dss/mersel-dss-server-signer-java) |

<br/>

## Katkıda Bulunma

Tüm projelerimiz **MIT lisansı** ile yayınlanmaktadır. Katkılarınızı bekliyoruz!

```
1. İlgili repoyu fork edin
2. Feature branch oluşturun
3. Pull Request açın
```

Sorularınız için ilgili repo'nun [Issues](https://github.com/orgs/mersel-os/repositories) bölümünü kullanabilirsiniz.

<br/>

---

<div align="center">

<sub>Mersel tarafından Türkiye'den, açık kaynak topluluğu için geliştirilmektedir.</sub>

<br/><br/>

[![mersel.io](https://img.shields.io/badge/mersel.io-0a0a0a?style=flat-square)](https://mersel.io)

</div>
