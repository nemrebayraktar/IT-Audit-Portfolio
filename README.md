# IT Audit Portfolio — Necdet Emre Bayraktar

![Role](https://img.shields.io/badge/Role-Information%20Systems%20Auditor-1f4e79)
![Focus](https://img.shields.io/badge/Focus-CISA%20oriented-2e7d32)
![Works](https://img.shields.io/badge/Audit%20works-10-555)
![Language](https://img.shields.io/badge/Reports-Turkish-c62828)

[🇹🇷 Türkçe](#-türkçe) · [🇬🇧 English](#-english)

---

## 🇹🇷 Türkçe

Merhaba, ben **Necdet Emre Bayraktar** — Bilgi Sistemleri Denetçisi. Bu repo, CISA odaklı bakış açısıyla kurgusal şirketler üzerinde yaptığım **10 uygulamalı BT denetimi** çalışmasını içerir. Her çalışmada yönetimin verdiği güvenceleri kabul etmek yerine teknik ve süreçsel kanıt topladım, beyan ile kanıtı karşılaştırdım, bulguları risk seviyesi ve kök neden analiziyle raporladım ve yönetime yönelik aksiyon önerileri hazırladım.

Kapsam; Linux ve Active Directory teknik denetimlerinden ISO 27001, DORA/NIS2 ve COBIT 2019 yönetişim ve uyum denetimlerine, veritabanı güvenliğine ve log/olay analizlerine kadar uzanır.

### Çalışmalar

| # | Kurum | Denetim Alanı | Çerçeve | Bulgu | Seviye | Klasör |
|---|---|---|---|---|---|---|
| 01 | **FinCore Bank** | Linux Sunucu Güvenlik Denetimi | Linux hardening · CIA · KVKK | 11 | 3 Kritik, 2 Yüksek risk kategorisi | [📂 Aç](01-FinCore-Bank-Linux-Server-Audit/) |
| 02 | **NordActive Holding** | Active Directory Yetkilendirme ve Erişim Denetimi | AD security · Least Privilege | 9 + 2 gözlem | 3 Critical · 6 High | [📂 Aç](02-NordActive-Holding-Active-Directory-Audit/) |
| 03 | **SecurePass Telecom** | Kimlik Doğrulama ve Active Directory Güvenlik Denetimi | IAM · Kerberos · Hash security | 9 | Tümü kritik bulgu (derecelendirmesiz) | [📂 Aç](03-SecurePass-Telecom-Identity-AD-Security-Audit/) |
| 04 | **MedGlobal Health** | ISO 27001 BGYS Denetimi | ISO/IEC 27001:2022 | 14 | 8 Critical · 6 High | [📂 Aç](04-MedGlobal-Health-ISO27001-ISMS-Audit/) |
| 05 | **EuroGrid Finance** | DORA & NIS2 Regülasyon Uyum Denetimi | DORA · NIS2 | 10 | 6 Critical · 4 High | [📂 Aç](05-EuroGrid-Finance-DORA-NIS2-Compliance-Audit/) |
| 06 | **Vertex Capital Group** | BT Yönetişimi ve İç Kontrol Denetimi | COBIT 2019 | 19 | 5 Critical · 12 High · 2 Medium | [📂 Aç](06-Vertex-Capital-Group-IT-Governance-COBIT-Audit/) |
| 07 | **DataVault Bank** | Oracle Veritabanı Güvenlik Denetimi | PCI-DSS · KVKK/GDPR · Oracle | 12 | 6 Critical · 6 High | [📂 Aç](07-DataVault-Bank-Oracle-Database-Security-Audit/) |
| 08 | **VolkanBank** | Erişim Yönetimi ve Parola Güvenliği Denetimi | IAM · MFA · Password hashing | 6 | Derecelendirme yok | [📂 Aç](08-VolkanBank-Access-Management-Audit/) |
| 09 | **VolkanBank** | İşlem Logu İzleme ve Olay Analizi | Log monitoring · RCA | 1 ana bulgu | — | [📂 Aç](09-VolkanBank-Transaction-Log-Monitoring-Analysis/) |
| 10 | **VolkanBank** | Kimlik Doğrulama Logu ve Olay Analizi | Log analysis · Incident response | 5 anormallik | — | [📂 Aç](10-VolkanBank-Authentication-Log-Incident-Analysis/) |

### Yetkinlikler ve çerçeveler
- **Standartlar ve regülasyonlar:** ISO/IEC 27001:2022, COBIT 2019, DORA, NIS2, PCI-DSS, KVKK / GDPR
- **Teknik denetim:** Linux sunucu hardening, Active Directory ve Kerberos, Oracle veritabanı güvenliği, AWS bulut gözlemleri
- **Denetim yöntemi:** yönetim beyanı ve kanıt karşılaştırması, çapraz doküman analizi, risk derecelendirme, Root Cause Analysis, Condition–Criteria–Cause–Effect bulgu yazımı
- **Analiz:** log korelasyonu, hash/parola analizi, olay (incident) analizi, KPI/KRI ve Yönetim Kurulu raporlama güvencesi
- **Raporlama:** yönetici özeti, risk tabloları, Yönetim Kurulu sunumu, 30/90/180 günlük aksiyon planları

### Repo yapısı
Her klasörde Türkçe denetim raporu (PDF), lab senaryosu ve ilgili kanıt dokümanları ile iki dilli bir `README.md` bulunur.

> ⚠️ **Sorumluluk reddi:** Tüm şirketler, kişiler, kullanıcı hesapları, IP adresleri, parolalar, hash'ler, kart numaraları ve diğer veriler eğitim amaçlı oluşturulmuş **kurgusal** verilerdir; gerçek bir kurumu, kişiyi veya üretim ortamını temsil etmez. Lab senaryoları bir eğitim programı kapsamında sağlanmıştır. Raporlar **Türkçe** yazılmıştır.

---

## 🇬🇧 English

Hi, I'm **Necdet Emre Bayraktar**, an Information Systems Auditor. This repository contains **10 hands-on IT audit engagements** on fictional companies, approached from a CISA-oriented perspective. In each one I collected technical and process evidence instead of accepting management's assurances, compared claims against evidence, reported findings with risk ratings and root cause analysis, and prepared management action plans.

The work ranges from technical Linux and Active Directory audits to ISO 27001, DORA/NIS2 and COBIT 2019 governance and compliance audits, database security, and log/incident analysis.

### Engagements

| # | Company | Audit Area | Framework | Findings | Severity | Folder |
|---|---|---|---|---|---|---|
| 01 | **FinCore Bank** | Linux Server Security Audit | Linux hardening · CIA · KVKK | 11 | 3 Critical, 2 High risk categories | [📂 Open](01-FinCore-Bank-Linux-Server-Audit/) |
| 02 | **NordActive Holding** | Active Directory Access & Privilege Audit | AD security · Least Privilege | 9 + 2 observations | 3 Critical · 6 High | [📂 Open](02-NordActive-Holding-Active-Directory-Audit/) |
| 03 | **SecurePass Telecom** | Authentication & Active Directory Security Audit | IAM · Kerberos · Hash security | 9 | All reported as critical (unrated) | [📂 Open](03-SecurePass-Telecom-Identity-AD-Security-Audit/) |
| 04 | **MedGlobal Health** | ISO/IEC 27001 ISMS Audit | ISO/IEC 27001:2022 | 14 | 8 Critical · 6 High | [📂 Open](04-MedGlobal-Health-ISO27001-ISMS-Audit/) |
| 05 | **EuroGrid Finance** | DORA & NIS2 Regulatory Compliance Audit | DORA · NIS2 | 10 | 6 Critical · 4 High | [📂 Open](05-EuroGrid-Finance-DORA-NIS2-Compliance-Audit/) |
| 06 | **Vertex Capital Group** | IT Governance & Internal Control Audit | COBIT 2019 | 19 | 5 Critical · 12 High · 2 Medium | [📂 Open](06-Vertex-Capital-Group-IT-Governance-COBIT-Audit/) |
| 07 | **DataVault Bank** | Oracle Database Security Audit | PCI-DSS · KVKK/GDPR · Oracle | 12 | 6 Critical · 6 High | [📂 Open](07-DataVault-Bank-Oracle-Database-Security-Audit/) |
| 08 | **VolkanBank** | Access Management & Password Security Audit | IAM · MFA · Password hashing | 6 | Not rated | [📂 Open](08-VolkanBank-Access-Management-Audit/) |
| 09 | **VolkanBank** | Transaction Log Monitoring & Incident Analysis | Log monitoring · RCA | 1 key finding | — | [📂 Open](09-VolkanBank-Transaction-Log-Monitoring-Analysis/) |
| 10 | **VolkanBank** | Authentication Log & Incident Analysis | Log analysis · Incident response | 5 anomalies | — | [📂 Open](10-VolkanBank-Authentication-Log-Incident-Analysis/) |

### Skills and frameworks
- **Standards & regulation:** ISO/IEC 27001:2022, COBIT 2019, DORA, NIS2, PCI-DSS, KVKK / GDPR
- **Technical auditing:** Linux server hardening, Active Directory & Kerberos, Oracle database security, AWS cloud observations
- **Audit methodology:** management assertion vs. evidence testing, cross-document analysis, risk rating, Root Cause Analysis, Condition–Criteria–Cause–Effect findings
- **Analysis:** log correlation, hash/password analysis, incident analysis, KPI/KRI and board-reporting assurance
- **Reporting:** executive summaries, risk tables, board briefings, 30/90/180-day action plans

### Repository layout
Each folder contains the Turkish audit report (PDF), the lab brief, relevant evidence documents and a bilingual `README.md`.

> ⚠️ **Disclaimer:** All companies, people, user accounts, IP addresses, passwords, hashes, card numbers and other data are **fictional** and were created for training purposes; they do not represent any real organisation, person or production environment. Lab scenarios were provided as part of a training programme. Reports are written in **Turkish**.
