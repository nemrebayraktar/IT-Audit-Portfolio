# 02 - NordActive Holding: Active Directory Access & Privilege Audit

Çerçeve / Framework: Least Privilege, AD security best practices, Condition–Criteria–Cause–Effect finding model

[Türkçe](#türkçe) | [English](#english)

## Türkçe

Denetim alanı: Active Directory Yetkilendirme ve Erişim Denetimi

### Benden istenen
Kurumsal Active Directory ortamında kullanıcı yaşam döngüsü, ayrıcalıklı hesaplar, Domain Admin üyelikleri, servis hesapları, parola ve kilitleme politikaları, GPO ve delegasyonlar, Kerberos ve hardening kontrollerini değerlendirmek; yönetim beyanlarını kanıt paketiyle (evidence pack, 3 Haziran 2026) karşılaştırarak bulgu raporu hazırlamak.

### Senaryo (kurgusal)
Yönetim; ayrılan çalışan hesaplarının zamanında kapatıldığını, Domain Admin üyeliklerinin minimum olduğunu, servis hesaplarının güvenli, GPO'ların standartlara uygun olduğunu ve ortamda kritik risk bulunmadığını beyan ediyor.

### Yöntem
10 yönetim beyanı tek tek kanıt referanslarıyla (EV-01 … EV-13) test edildi. Her bulgu profesyonel denetim formatında yazıldı: Condition, Criteria, Risk / Impact, Root Cause, Evidence, Recommendation, Risk Rating ve Management Action / Owner (termin dahil). Telafi edici kontroller ayrıca gözlem olarak raporlandı.

### Temel bulgular
9 bulgu: 3 Critical, 6 High ve 2 gözlem. Öne çıkanlar: sözleşmesi 14 ay önce bitmiş taşeron hesabıyla yakın zamanda giriş yapılması (aktif ihlal şüphesi), Domain Admins üyesi ve RC4 kullanan servis hesabı (Kerberoasting), Helpdesk grubunun Default Domain Policy'yi değiştirebilmesi, tek Domain Controller, kapatılmayan ayrılan personel hesapları, kapalı hesap kilitleme ve desteklenmeyen Windows Server 2012 R2.

### Kullanılan yetkinlikler
Active Directory denetimi / AD auditing · Privileged access · Kerberos riskleri / Kerberos risks · Evidence referencing · Management action plans

### Dosyalar
- [NordActive-Holding-Audit-Report-TR.pdf](NordActive-Holding-Audit-Report-TR.pdf): Denetim raporu
- [Lab-Brief-TR.pdf](Lab-Brief-TR.pdf): Lab senaryosu
- [evidence/AD-Audit-Evidence-Pack.pdf](evidence/AD-Audit-Evidence-Pack.pdf): Kanıt paketi
- [evidence/AD-Console-Screens.pdf](evidence/AD-Console-Screens.pdf): AD ekran kanıtları

Not: Bu çalışmadaki şirket, kişi, hesap, IP ve diğer tüm veriler eğitim için oluşturulmuş kurgusal verilerdir. Rapor Türkçedir.

## English

Audit area: Active Directory Access & Privilege Audit

### What I was asked to do
Assess user lifecycle, privileged accounts, Domain Admin membership, service accounts, password and lockout policy, GPOs and delegations, Kerberos and hardening in an enterprise Active Directory; compare management assertions with the evidence pack (cut-off 3 June 2026) and produce a findings report.

### Scenario (fictional)
Management asserts that leaver accounts are closed on time, Domain Admin membership is minimal, service accounts are secure, GPOs follow standards and there is no critical risk in the environment.

### Methodology
Each of the 10 management assertions was tested against evidence references (EV-01 … EV-13). Findings follow a professional audit format: Condition, Criteria, Risk / Impact, Root Cause, Evidence, Recommendation, Risk Rating and Management Action / Owner with due dates. Compensating controls were reported separately as observations.

### Key findings
9 findings: 3 Critical, 6 High, plus 2 observations. Highlights: recent logon with a contractor account expired 14 months earlier (suspected active breach), a Domain Admin service account using RC4 (Kerberoasting), Helpdesk able to modify the Default Domain Policy, a single Domain Controller, active leaver accounts, account lockout disabled and an end-of-life Windows Server 2012 R2.

### Skills used
Active Directory denetimi / AD auditing · Privileged access · Kerberos riskleri / Kerberos risks · Evidence referencing · Management action plans

### Files
- [NordActive-Holding-Audit-Report-TR.pdf](NordActive-Holding-Audit-Report-TR.pdf): Audit report
- [Lab-Brief-TR.pdf](Lab-Brief-TR.pdf): Lab brief
- [evidence/AD-Audit-Evidence-Pack.pdf](evidence/AD-Audit-Evidence-Pack.pdf): Evidence pack
- [evidence/AD-Console-Screens.pdf](evidence/AD-Console-Screens.pdf): AD console screen evidence

Note: All companies, people, accounts, IPs and other data in this work are fictional and were created for training. The report is in Turkish.

---
[Ana sayfa / Back to main page](../README.md)
