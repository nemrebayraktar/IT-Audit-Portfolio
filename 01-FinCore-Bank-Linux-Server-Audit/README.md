# 01 - FinCore Bank: Linux Server Security Audit

Çerçeve / Framework: Linux hardening, CIA Triad, Defense in Depth, KVKK

[Türkçe](#türkçe) | [English](#english)

## Türkçe

Denetim alanı: Linux Sunucu Güvenlik Denetimi

### Benden istenen
İnternete açık, AWS üzerinde çalışan kritik bir Amazon Linux 2023 sunucusunu salt okunur (read-only) bir hesapla teknik olarak incelemek; kullanıcı/grup yönetimi, yetkilendirme, SSH, parola politikaları, hassas veri, dosya izinleri, log, patch, servisler ve hardening başlıklarında riskleri kanıtlarıyla raporlamak. İstenen bölümler: Yönetici Özeti, Denetim Kapsamı, Yapılan Testler, Tespit Edilen Bulgular, Risk Değerlendirmesi, Öneriler.

### Senaryo (kurgusal)
Sistem sahipleri sunucuda hassas veri, gereksiz hesap veya yapılandırma hatası bulunmadığını; parola ve SSH politikalarının güçlü, sistemin güncel olduğunu beyan ediyor.

### Yöntem
Sunucuya bağlanılarak `uptime`, `last`, `lastlog`, `w`, `chage`, `sudo -l`, `systemctl`, `sshd_config` incelemesi, `dnf check-update` ve `find -perm` ile dosya izin taramaları yapıldı. Her yönetim beyanı komut çıktısıyla karşılaştırıldı; saha notları ayrı bir dokümanda tutuldu ve rapor, brief'te istenen altı bölüm yapısında hazırlandı.

### Temel bulgular
5 alanda 11 bulgu; risk tablosunda 3 Kritik, 2 Yüksek risk kategorisi. Öne çıkanlar: `test` hesabında `NOPASSWD: ALL` sudo yetkisi, müşteri verisi, maaşlar ve AWS anahtarları dahil kritik dosyaların `777` izinli olması, internete açık şifresiz FTP, host firewall yokluğu, `auditd`'nin başlangıçta kapalı olması, parola yaşlandırmasının olmaması ve atıl/paylaşımlı hesaplar.

### Kullanılan yetkinlikler
Linux güvenlik denetimi / Linux security auditing · IAM · Hardening · Patch & log management · Risk değerlendirmesi / risk rating

### Dosyalar
- [FinCore-Bank-Audit-Report-TR.pdf](FinCore-Bank-Audit-Report-TR.pdf): Denetim raporu
- [Lab-Brief-TR.pdf](Lab-Brief-TR.pdf): Lab senaryosu
- [working-notes/Audit-Field-Notes-TR.pdf](working-notes/Audit-Field-Notes-TR.pdf): Denetim sırasında tutulan saha notları

Not: Bu çalışmadaki şirket, kişi, hesap, IP ve diğer tüm veriler eğitim için oluşturulmuş kurgusal verilerdir. Rapor Türkçedir.

## English

Audit area: Linux Server Security Audit

### What I was asked to do
Technically review a critical, internet-facing Amazon Linux 2023 server on AWS using a read-only account, and report evidence-backed risks across user/group management, privileges, SSH, password policy, sensitive data, file permissions, logging, patching, services and hardening. Required sections: Executive Summary, Scope, Tests Performed, Findings, Risk Assessment, Recommendations.

### Scenario (fictional)
System owners claim the server holds no sensitive data, has no unnecessary accounts or misconfigurations, and that password/SSH policies are strong and the OS is up to date.

### Methodology
Hands-on review over SSH: `uptime`, `last`, `lastlog`, `w`, `chage`, `sudo -l`, `systemctl`, `sshd_config` review, `dnf check-update` and `find -perm` permission sweeps. Each management claim was tested against command output; field notes were kept separately and the report follows the six sections required by the brief.

### Key findings
11 findings across 5 areas; risk table rates 3 Critical and 2 High risk categories. Highlights: `NOPASSWD: ALL` sudo on a `test` account, world-writable (`777`) files containing customer data, salaries and AWS keys, internet-exposed cleartext FTP, no host firewall, `auditd` disabled at boot, no password aging, dormant and shared accounts.

### Skills used
Linux güvenlik denetimi / Linux security auditing · IAM · Hardening · Patch & log management · Risk değerlendirmesi / risk rating

### Files
- [FinCore-Bank-Audit-Report-TR.pdf](FinCore-Bank-Audit-Report-TR.pdf): Audit report
- [Lab-Brief-TR.pdf](Lab-Brief-TR.pdf): Lab brief
- [working-notes/Audit-Field-Notes-TR.pdf](working-notes/Audit-Field-Notes-TR.pdf): Field notes taken during the audit

Note: All companies, people, accounts, IPs and other data in this work are fictional and were created for training. The report is in Turkish.

---
[Ana sayfa / Back to main page](../README.md)
