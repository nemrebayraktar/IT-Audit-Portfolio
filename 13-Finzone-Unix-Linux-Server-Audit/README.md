# 13 - Finzone: Unix / Linux Sunucu Güvenlik Denetimi

Türkçe | [English](#english)

Denetim alanı: Linux sunucu güvenliği (db-prod-01, Ubuntu 22.04.4 LTS)
Çerçeve: ISO/IEC 27001, COBIT 2019

## Benden istenen

Bir üretim veritabanı sunucusunda ISO 27001 uyumluluğunu değerlendirmek, güvenlik açıklarını bulmak ve politika, prosedür ve teknik kontrolleri komut çıktılarıyla doğrulamak.

## Nasıl yaptım

İncelemeyi 7 başlıkta yaptım: politika ve prosedür, kullanıcı envanteri, SSH yapılandırması, güncel olmayan paketler, yetki yönetimi, servisler ve zaman / loglama. Her başlıkta ilgili komutu çalıştırıp çıktıyı kanıt olarak kullandım (hostnamectl, getent passwd ve HR listesiyle comm karşılaştırması, sshd -T, auth.log, apt list --upgradable, sudo -l, systemctl, find -perm -0002, timedatectl, rsyslog). Her alanı Uygun / Kısmen / Uygun Değil olarak değerlendirdim. Tek tek eksikleri yazmak yerine, arkasındaki süreç eksikliğini (kullanıcı yaşam döngüsü, yama yönetimi) raporlamaya çalıştım.

## Sonuç

5 bulgu ve 2 gözlem: 3 High, 2 Medium. HR listesinde olmayan aktif "ops" hesabı, bekleyen OpenSSH / OpenSSL güvenlik güncellemeleri, bu hesaba tanımlı ve journalctl üzerinden root shell'e açılabilen sudo yetkisi, herkesin yazabildiği bir uygulama dizini ve politika dokümanlarının onay / güncellik kanıtının olmaması. SSH ve NTP kontrolleri uygun bulundu; merkezi loglama var ancak log bütünlüğü ve alarm kanıtı sunulmadı.

## Dosyalar

- [Finzone-Unix-Audit-Report-TR.pdf](Finzone-Unix-Audit-Report-TR.pdf) - Denetim raporu (Türkçe)

Bu çalışmadaki şirket, sunucu, kullanıcı ve IP bilgileri eğitim amaçlı ve kurgusaldır (IP'ler dokümantasyon için ayrılmış bloklardandır).

---

## English

Audit area: Linux server security (db-prod-01, Ubuntu 22.04.4 LTS)
Frameworks: ISO/IEC 27001, COBIT 2019

What I was asked to do: assess ISO 27001 compliance on a production database server, identify vulnerabilities and verify policies, procedures and technical controls using command output as evidence.

How I did it: seven areas (policy and procedure, user inventory, SSH, outdated packages, privilege management, services, time and logging), each tested with the relevant command and rated Compliant / Partial / Not compliant. I tried to report the process gap behind each issue (user lifecycle, patch management), not just the single missing item.

Result: 5 findings and 2 observations, 3 High, 2 Medium: an active "ops" account not on the HR list, pending OpenSSH / OpenSSL security updates, sudo rules for that account that allow a root shell via journalctl's pager, a world-writable application directory, and no evidence of approval or review for the policy documents. SSH and NTP were found compliant; logs are centralised but there was no evidence of log integrity or alerting.

The report is written in Turkish. All data is fictional.

[Portföy ana sayfası / Back to portfolio](../README.md)
