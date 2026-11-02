# 11 - NextCorp: Bilgi Güvenliği ve BT Altyapısı Denetimi

Türkçe | [English](#english)

Denetim alanı: BT altyapısı, kimlik ve erişim yönetimi, veri güvenliği
Çerçeve: ISO/IEC 27001:2013 Ek A

## Benden istenen

AWS, şirket içi sunucular, Google Workspace ve NextID kimlik platformundan oluşan hibrit bir yapıya sahip, ISO 27001 sertifikasyonu hedefleyen bir şirketin altyapısını incelemek, eksiklikleri bulmak ve her biri için neden, etki ve öneri yazmak.

## Senaryo (kurgusal)

Şirkette dosyalar USB ve Google Drive ile paylaşılıyor, maaşlar Excel'de tutuluyor, yedekler haftalık olarak elle USB'ye alınıyor. Cihazların bir kısmı ve bazı sunucular desteği bitmiş işletim sistemleriyle çalışıyor. NextID platformunda kullanıcılar, MFA durumları ve erişim yetkileri; Ubuntu web sunucusunda ise kullanıcılar, SSH ve güvenlik duvarı ayarları inceleniyor.

## Nasıl yaptım

Önce yönetime sorulacak soruları hazırladım (raporun Ek-1 bölümünde). Sonra işletim sistemi envanterini, NextID kullanıcı listesini, Ubuntu sunucuda SSH, ufw, otomatik güncelleme, sudo sürümü, /etc/passwd ve /etc/shadow bilgilerini, Fatura Onay Sistemi ve İK Portalı yetkilerini inceledim. Her bulguyu ISO 27001 Ek A kontrolüyle eşleştirip Eksiklik / Neden / Etki / Öneri ve risk seviyesiyle yazdım, sonunda risk tablosu ve 30/90/180 günlük aksiyon planı ekledim.

## Sonuç

15 bulgu: 3 Critical, 9 High, 3 Medium. Öne çıkanlar: IT yöneticisi ve servis hesabında MFA olmaması, işten ayrılan bir personelin hesabının AWS ve sunucuda hala açık olması, desteği bitmiş Windows / Ubuntu sistemleri, maaş verilerinin korumasız Excel dosyalarında tutulması, fatura sisteminde aynı kişinin hem oluşturup hem onaylayabilmesi (SoD) parolaların MD5-crypt ile saklanması ve aynı kullanıcının bir sistemde IT Admin, diğerinde Yazılım Geliştirici olarak tanımlı olması (ayrıcalıklı erişim, SoD ve hesap verebilirlik ihlali).

## Dosyalar

- [NextCorp-Audit-Report-TR.pdf](NextCorp-Audit-Report-TR.pdf) - Denetim raporu (Türkçe)

Bu çalışmadaki şirket, kullanıcı adları ve tüm veriler eğitim amaçlı ve kurgusaldır.

---

## English

Audit area: IT infrastructure, identity and access management, data security
Framework: ISO/IEC 27001:2013 Annex A

What I was asked to do: review the infrastructure of a company with a hybrid setup (AWS, on-prem servers, Google Workspace and the NextID identity platform) that is aiming for ISO 27001 certification, identify gaps and write the cause, impact and recommendation for each.

Scenario (fictional): files are shared over USB and Google Drive, payroll is kept in Excel, backups are taken weekly to USB by hand, and some devices and servers run end-of-life operating systems. User accounts, MFA and access rights are reviewed on NextID; users, SSH and firewall settings on the Ubuntu web server.

How I did it: I first prepared the questions for management (Appendix 1 of the report). Then I reviewed the OS inventory, the NextID user list, SSH / ufw / auto-update / sudo version and /etc/passwd and /etc/shadow on the Ubuntu server, and the permissions in the invoice approval system and the HR portal. Each finding is mapped to an ISO 27001 Annex A control and written as Gap / Cause / Impact / Recommendation with a risk rating, followed by a risk table and a 30/90/180-day action plan.

Result: 15 findings, 3 Critical, 9 High, 3 Medium. Key issues: no MFA on the IT admin and a service account, a leaver's account still active on AWS and the server, end-of-life Windows / Ubuntu systems, payroll data in unprotected Excel files, one user able to both create and approve invoices (SoD), passwords stored with MD5-crypt, and the same user defined as IT Admin in one system and Developer in another (privileged access, SoD and accountability issue).

The report is written in Turkish. All companies, usernames and data are fictional and created for training.

[Portföy ana sayfası / Back to portfolio](../README.md)
