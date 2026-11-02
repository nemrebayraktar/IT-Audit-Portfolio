# 03 · SecurePass Telecom — Authentication & Active Directory Security Audit

`Identity · Hash Analysis · Kerberos` · **Framework:** Least Privilege, password & hash security, Kerberos (Kerberoasting / AS-REP Roasting), IAM & SoD

[🇹🇷 Türkçe](#-türkçe) · [🇬🇧 English](#-english)

---

## 🇹🇷 Türkçe

**Denetim alanı:** Kimlik Doğrulama ve Active Directory Güvenlik Denetimi

### Benden istenen
Sağlanan kanıtlar (kullanıcı listeleri, parola politikası, MFA raporu, servis hesapları, hash dökümleri, Kerberos ve kimlik doğrulama logları) üzerinden kimlik doğrulama kontrollerini, parola güvenliğini ve ayrıcalıklı erişimleri değerlendirmek ve kanıta dayalı kısa bir denetim raporu hazırlamak.

### Senaryo (kurgusal)
Sistem sahipleri parola politikalarının sektör standartlarında olduğunu, MFA'nın kritik hesaplarda aktif olduğunu, kullanılmayan hesap bulunmadığını, hash algoritmalarının ve Kerberos yapılandırmasının güvenli olduğunu beyan ediyor (11 güvence).

### Yöntem
Event ID bazlı log analizi, NTLM/MD5/SHA256 hash analizi (zayıf parolaların doğrulanması), AS-REP Roasting ve Kerberoasting riski analizi, IAM ve görevler ayrılığı incelemesi yapıldı. Her güvence kanıtla karşılaştırıldı; ayrıca "yalnızca backupsvc ele geçirilirse ne olur?" saldırı senaryosu modellendi.

### Temel bulgular
**9 kritik bulgu** ve 6 maddelik öneri planı (raporda ayrıca seviye derecelendirmesi yok). Öne çıkanlar: karmaşıklık kapalı, kilitleme eşiği 0 ve geri döndürülebilir şifreleme açık; yönetici ve servis hesaplarında kırılabilir zayıf parolalar; ayrıcalıklı hesaplarda MFA yok; servis ve dış danışman hesapları Domain Admins grubunda; aynı IP'den insan ve servis hesaplarıyla başarılı girişler (yanal hareket şüphesi).

### Gösterilen yetkinlikler
Hash analizi / hash analysis (Hashcat) · Kerberos saldırı yüzeyi / Kerberos attack surface · Log analizi / log analysis · Attack-path thinking

### Dosyalar
- [`SecurePass-Telecom-Audit-Report-TR.pdf`](SecurePass-Telecom-Audit-Report-TR.pdf) — Denetim raporu
- [`Lab-Brief-and-Evidence-TR.pdf`](Lab-Brief-and-Evidence-TR.pdf) — Lab senaryosu ve kanıtlar
- [`working-notes/Audit-Review-Notes-TR.pdf`](working-notes/Audit-Review-Notes-TR.pdf) — İnceleme notları
- [`reference/AD-Auditor-Toolkit-TR.pdf`](reference/AD-Auditor-Toolkit-TR.pdf) — AD denetçi araç kutusu (referans)

> ⚠️ Bu çalışmadaki şirket, kişi, kullanıcı, IP ve tüm veriler eğitim amaçlı oluşturulmuş **kurgusal** verilerdir; gerçek bir kurumu temsil etmez. Rapor dili Türkçedir.

---

## 🇬🇧 English

**Audit area:** Authentication & Active Directory Security Audit

### What I was asked to do
Using the provided evidence (user lists, password policy, MFA report, service accounts, hash dumps, Kerberos and authentication logs), evaluate authentication controls, password security and privileged access, and write a short evidence-based audit report.

### Scenario (fictional)
System owners claim industry-standard password policies, MFA on critical accounts, no unused accounts, and secure hash algorithms and Kerberos configuration (11 assurances).

### Methodology
Event-ID based log analysis, NTLM/MD5/SHA256 hash analysis (confirming weak passwords), AS-REP Roasting and Kerberoasting exposure review, IAM and segregation-of-duties review. Each assurance was tested against evidence, and an attack path ("what if only backupsvc is compromised?") was modelled.

### Key findings
**9 critical findings** and a 6-point recommendation plan (no separate severity scale in the report). Highlights: complexity disabled, lockout threshold 0 and reversible encryption enabled; crackable weak passwords on admin and service accounts; no MFA on privileged accounts; service and external consultant accounts in Domain Admins; successful logons from one IP with both human and service accounts (suspected lateral movement).

### Skills demonstrated
Hash analizi / hash analysis (Hashcat) · Kerberos saldırı yüzeyi / Kerberos attack surface · Log analizi / log analysis · Attack-path thinking

### Files
- [`SecurePass-Telecom-Audit-Report-TR.pdf`](SecurePass-Telecom-Audit-Report-TR.pdf) — Audit report
- [`Lab-Brief-and-Evidence-TR.pdf`](Lab-Brief-and-Evidence-TR.pdf) — Lab brief and evidence
- [`working-notes/Audit-Review-Notes-TR.pdf`](working-notes/Audit-Review-Notes-TR.pdf) — Review notes
- [`reference/AD-Auditor-Toolkit-TR.pdf`](reference/AD-Auditor-Toolkit-TR.pdf) — AD auditor toolkit (reference)

> ⚠️ All companies, people, accounts, IPs and data in this work are **fictional** and created for training; they do not represent any real organisation. The report is written in Turkish.

---
[⬅ Portföy ana sayfası / Back to portfolio](../README.md)
