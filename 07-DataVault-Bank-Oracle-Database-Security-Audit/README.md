# 07 - DataVault Bank: Oracle Database Security Audit

Çerçeve / Framework: Least Privilege, SoD, PCI-DSS, KVKK/GDPR, Oracle security best practices

[Türkçe](#türkçe) | [English](#english)

## Türkçe

Denetim alanı: Oracle Veritabanı Güvenlik Denetimi

### Benden istenen
Kritik müşteri verilerini barındıran Oracle 19c üretim veritabanını (DATAVAULTPRD) yalnızca paylaşılan sorgu çıktıları üzerinden denetlemek, riskleri belirlemek ve denetim raporu hazırlamak.

### Senaryo (kurgusal)
Veritabanı yöneticileri yetkilerin minimum, hassas verilerin korunduğunu ve şifrelendiğini, ayrıcalıklı erişimlerin gözden geçirildiğini, veritabanının güncel, loglamanın etkin, görevler ayrılığının uygulandığını ve varsayılan hesapların kapatıldığını beyan ediyor (8 güvence).

### Yöntem
`dba_users`, `dba_role_privs`, `dba_sys_privs`, `dba_profiles`, parola hash sürümleri, `dba_tablespaces`, örnek veri, audit parametreleri, RMAN yapılandırması, `v$instance`, `dba_db_links`, başarısız girişler, aktif oturumlar ve değişiklik kayıtları incelendi. 8 güvence kanıtla karşılaştırıldı; her bulgu Durum / Risk / Öneri / Risk Seviyesi formatında yazıldı ve risk tablosu hazırlandı.

### Temel bulgular
12 bulgu: 6 Critical, 6 High. 8 güvencenin hiçbiri kanıtla doğrulanamadı. Öne çıkanlar: uygulama, rapor, geliştirici ve danışman hesaplarında DBA rolü; sınırsız deneme hakkı ve SYS'e 324 başarısız giriş; şifrelenmemiş tablespace'ler ve maskelenmemiş kredi kartı / T.C. Kimlik No verileri; `audit_trail = NONE`; 17 Kasım 2025'ten beri yedek yok; yamasız 19.3.0.0; SYS kullanan database link; onaysız canlı değişiklikler.

### Kullanılan yetkinlikler
Database security auditing · Oracle · Privileged access · Encryption & data masking · PCI-DSS / KVKK

### Dosyalar
- [DataVault-Bank-Audit-Report-TR.pdf](DataVault-Bank-Audit-Report-TR.pdf): Denetim raporu
- [Lab-Brief-and-Evidence-TR.pdf](Lab-Brief-and-Evidence-TR.pdf): Lab senaryosu ve sorgu çıktıları

Not: Bu çalışmadaki şirket, kişi, hesap, IP ve diğer tüm veriler eğitim için oluşturulmuş kurgusal verilerdir. Rapor Türkçedir.

## English

Audit area: Oracle Database Security Audit

### What I was asked to do
Audit the Oracle 19c production database (DATAVAULTPRD) holding critical customer data using only the query outputs provided, identify risks and write an audit report.

### Scenario (fictional)
DBAs claim minimal privileges, protected and encrypted sensitive data, reviewed privileged access, an up-to-date database, active logging, segregation of duties and disabled default accounts (8 assurances).

### Methodology
Reviewed `dba_users`, `dba_role_privs`, `dba_sys_privs`, `dba_profiles`, password hash versions, `dba_tablespaces`, sample data, audit parameters, RMAN configuration, `v$instance`, `dba_db_links`, failed logins, active sessions and the change log. The 8 assurances were tested against evidence; each finding uses Condition / Risk / Recommendation / Risk Level, with a summary risk table.

### Key findings
12 findings: 6 Critical, 6 High. None of the 8 assurances could be verified. Highlights: DBA role on application, reporting, developer and consultant accounts; unlimited login attempts and 324 failed logins on SYS; unencrypted tablespaces and unmasked card / national ID data; `audit_trail = NONE`; no backup since 17 Nov 2025; unpatched 19.3.0.0; a database link using SYS; unapproved production changes.

### Skills used
Database security auditing · Oracle · Privileged access · Encryption & data masking · PCI-DSS / KVKK

### Files
- [DataVault-Bank-Audit-Report-TR.pdf](DataVault-Bank-Audit-Report-TR.pdf): Audit report
- [Lab-Brief-and-Evidence-TR.pdf](Lab-Brief-and-Evidence-TR.pdf): Lab brief and query outputs

Note: All companies, people, accounts, IPs and other data in this work are fictional and were created for training. The report is in Turkish.

---
[Ana sayfa / Back to main page](../README.md)
