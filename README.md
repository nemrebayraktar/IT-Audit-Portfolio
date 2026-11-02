# IT Audit Portfolio - Necdet Emre Bayraktar

[Türkçe](#türkçe) | [English](#english)

## Türkçe

Ben Necdet Emre Bayraktar, bilgi sistemleri denetçisi adayıyım ve CISA sınavına hazırlanıyorum. Bu repoda kurgusal şirketler üzerinde yaptığım 10 BT denetimi çalışması var. Her çalışmada yönetimin beyanlarını kanıtlarla karşılaştırdım. Bulguları risk seviyesi ve kök nedenleriyle raporladım, yönetim için aksiyon önerileri yazdım.

Çalışmalar Linux ve Active Directory teknik denetimlerinden ISO 27001, DORA/NIS2 ve COBIT 2019 uyum ve yönetişim denetimlerine, veritabanı güvenliğine ve log analizine kadar uzanıyor.

### Çalışmalar

| # | Kurum | Denetim alanı | Çerçeve | Bulgu | Seviye |
|---|---|---|---|---|---|
| 01 | [FinCore Bank](01-FinCore-Bank-Linux-Server-Audit/) | Linux Sunucu Güvenlik Denetimi | Linux hardening · CIA · KVKK | 11 | 3 Kritik, 2 Yüksek risk kategorisi |
| 02 | [NordActive Holding](02-NordActive-Holding-Active-Directory-Audit/) | Active Directory Yetkilendirme ve Erişim Denetimi | AD security · Least Privilege | 9 + 2 gözlem | 3 Critical · 6 High |
| 03 | [SecurePass Telecom](03-SecurePass-Telecom-Identity-AD-Security-Audit/) | Kimlik Doğrulama ve Active Directory Güvenlik Denetimi | IAM · Kerberos · Hash security | 9 | Tümü kritik bulgu (derecelendirmesiz) |
| 04 | [MedGlobal Health](04-MedGlobal-Health-ISO27001-ISMS-Audit/) | ISO 27001 BGYS Denetimi | ISO/IEC 27001:2022 | 14 | 8 Critical · 6 High |
| 05 | [EuroGrid Finance](05-EuroGrid-Finance-DORA-NIS2-Compliance-Audit/) | DORA & NIS2 Regülasyon Uyum Denetimi | DORA · NIS2 | 10 | 6 Critical · 4 High |
| 06 | [Vertex Capital Group](06-Vertex-Capital-Group-IT-Governance-COBIT-Audit/) | BT Yönetişimi ve İç Kontrol Denetimi | COBIT 2019 | 19 | 5 Critical · 12 High · 2 Medium |
| 07 | [DataVault Bank](07-DataVault-Bank-Oracle-Database-Security-Audit/) | Oracle Veritabanı Güvenlik Denetimi | PCI-DSS · KVKK/GDPR · Oracle | 12 | 6 Critical · 6 High |
| 08 | [VolkanBank](08-VolkanBank-Access-Management-Audit/) | Erişim Yönetimi ve Parola Güvenliği Denetimi | IAM · MFA · Password hashing | 6 | Derecelendirme yok |
| 09 | [VolkanBank](09-VolkanBank-Transaction-Log-Monitoring-Analysis/) | İşlem Logu İzleme ve Olay Analizi | Log monitoring · RCA | 1 ana bulgu | — |
| 10 | [VolkanBank](10-VolkanBank-Authentication-Log-Incident-Analysis/) | Kimlik Doğrulama Logu ve Olay Analizi | Log analysis · Incident response | 5 anormallik | — |

### Kullandığım çerçeveler ve yöntemler
- Standartlar ve regülasyonlar: ISO/IEC 27001:2022, COBIT 2019, DORA, NIS2, PCI-DSS, KVKK / GDPR
- Teknik denetim: Linux sunucu hardening, Active Directory ve Kerberos, Oracle veritabanı güvenliği, AWS
- Denetim yöntemi: beyan ve kanıt karşılaştırması, dokümanlar arası çapraz kontrol, risk derecelendirme, kök neden analizi
- Analiz: log korelasyonu, hash ve parola analizi, olay analizi, KPI/KRI ve yönetim kurulu raporlarının doğrulanması
- Raporlama: yönetici özeti, risk tabloları, yönetim kurulu sunumu, 30/90/180 günlük aksiyon planları

### Repo yapısı
Her klasörde Türkçe denetim raporu (PDF), lab senaryosu, ilgili kanıt dokümanları ve iki dilli bir README var.

Not: Tüm şirketler, kişiler, hesaplar, IP adresleri, parolalar, hash'ler, kart numaraları ve diğer veriler eğitim için oluşturulmuş kurgusal verilerdir. Gerçek bir kurumu, kişiyi veya sistemi temsil etmez. Lab senaryoları bir eğitim programı kapsamında verildi. Raporlar Türkçedir.

## English

I'm Necdet Emre Bayraktar, an aspiring information systems auditor preparing for the CISA exam. This repository contains 10 IT audit exercises I did on fictional companies. In each one I compared management's claims with the evidence. I reported findings with risk levels and root causes, and wrote action points for management.

The work covers technical Linux and Active Directory audits, ISO 27001, DORA/NIS2 and COBIT 2019 compliance and governance audits, database security and log analysis.

### Engagements

| # | Company | Audit area | Framework | Findings | Severity |
|---|---|---|---|---|---|
| 01 | [FinCore Bank](01-FinCore-Bank-Linux-Server-Audit/) | Linux Server Security Audit | Linux hardening · CIA · KVKK | 11 | 3 Critical, 2 High risk categories |
| 02 | [NordActive Holding](02-NordActive-Holding-Active-Directory-Audit/) | Active Directory Access & Privilege Audit | AD security · Least Privilege | 9 + 2 observations | 3 Critical · 6 High |
| 03 | [SecurePass Telecom](03-SecurePass-Telecom-Identity-AD-Security-Audit/) | Authentication & Active Directory Security Audit | IAM · Kerberos · Hash security | 9 | All reported as critical (unrated) |
| 04 | [MedGlobal Health](04-MedGlobal-Health-ISO27001-ISMS-Audit/) | ISO/IEC 27001 ISMS Audit | ISO/IEC 27001:2022 | 14 | 8 Critical · 6 High |
| 05 | [EuroGrid Finance](05-EuroGrid-Finance-DORA-NIS2-Compliance-Audit/) | DORA & NIS2 Regulatory Compliance Audit | DORA · NIS2 | 10 | 6 Critical · 4 High |
| 06 | [Vertex Capital Group](06-Vertex-Capital-Group-IT-Governance-COBIT-Audit/) | IT Governance & Internal Control Audit | COBIT 2019 | 19 | 5 Critical · 12 High · 2 Medium |
| 07 | [DataVault Bank](07-DataVault-Bank-Oracle-Database-Security-Audit/) | Oracle Database Security Audit | PCI-DSS · KVKK/GDPR · Oracle | 12 | 6 Critical · 6 High |
| 08 | [VolkanBank](08-VolkanBank-Access-Management-Audit/) | Access Management & Password Security Audit | IAM · MFA · Password hashing | 6 | Not rated |
| 09 | [VolkanBank](09-VolkanBank-Transaction-Log-Monitoring-Analysis/) | Transaction Log Monitoring & Incident Analysis | Log monitoring · RCA | 1 key finding | — |
| 10 | [VolkanBank](10-VolkanBank-Authentication-Log-Incident-Analysis/) | Authentication Log & Incident Analysis | Log analysis · Incident response | 5 anomalies | — |

### Frameworks and methods
- Standards and regulation: ISO/IEC 27001:2022, COBIT 2019, DORA, NIS2, PCI-DSS, KVKK / GDPR
- Technical auditing: Linux server hardening, Active Directory and Kerberos, Oracle database security, AWS
- Audit approach: testing management claims against evidence, cross-checking documents, risk rating, root cause analysis
- Analysis: log correlation, hash and password analysis, incident analysis, checking KPI/KRI and board reports
- Reporting: executive summaries, risk tables, board briefings, 30/90/180-day action plans

### Repository layout
Each folder has the Turkish audit report (PDF), the lab brief, related evidence documents and a bilingual README.

Note: All companies, people, accounts, IP addresses, passwords, hashes, card numbers and other data are fictional and were created for training. They do not represent any real organisation, person or system. The lab scenarios were provided as part of a training programme. Reports are in Turkish.
