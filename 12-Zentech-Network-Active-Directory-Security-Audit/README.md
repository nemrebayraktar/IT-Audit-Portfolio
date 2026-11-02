# 12 - Zentech Bilişim: Ağ ve Active Directory Güvenlik Denetimi

Türkçe | [English](#english)

Denetim alanı: Active Directory, ağ cihazları, VLAN segmentasyonu, parola güvenliği
Dayanak: Şirketin kendi Bilgi Güvenliği Politikası ve Parola Politikası

## Benden istenen

70 çalışanlı, İstanbul merkezli bir yazılım firmasının BT altyapısını şirketin kendi yazılı politikalarıyla karşılaştırmak; eksik bilgileri sorularla tamamlamak ve bulguları Eksiklik / Neden / Etki / Öneri şeklinde raporlamak.

## Senaryo (kurgusal)

Ortamda 1 Domain Controller (zentech.local), 2 fiziksel sunucu, 6 switch (Cisco, TP-Link, Ubiquiti, Zyxel), 2 Wi-Fi erişim noktası, 3 VLAN (Admin, Developer, Guest) ve bir Cisco ASA 5505 firewall var. IT personeli güçlü parola kullandığını ve parola politikasının uygulandığını söylüyor.

## Nasıl yaptım

Önce eksik bilgiler için soru listesi hazırladım (raporun Ek-1 bölümünde), örneğin Wi-Fi ağlarının hangi VLAN'a çıktığı. Switch üzerindeki /etc/shadow dosyasından alınan root hash'ini Hashcat ile test ettim; hash tuzsuz SHA-1 çıktı ve parola "admin123" olarak kırıldı. Domain Admins grubunu, Guest hesabını, Audit Policy ve GPO ayarlarını, VLAN yapısını ve cihaz sürümlerini politikalarla karşılaştırdım.

## Sonuç

6 bulgu: 3 Critical, 3 High. Kırılan switch root parolası, Domain Admins grubunda yönetici olmaması gereken kullanıcılar, parolasız aktif Guest hesabı, kapalı Audit Policy ve GPO ile zorunlu kılınmayan parola politikası, belirsiz VLAN ayrımı ve güncelleme almayan ağ cihazları (Zyxel switch, IOS 12.2, ASA 8.2(5)).

## Dosyalar

- [Zentech-Audit-Report-TR.pdf](Zentech-Audit-Report-TR.pdf) - Denetim raporu (Türkçe)

Bu çalışmadaki şirket, kullanıcı adları, parola ve hash değerleri eğitim amaçlı ve kurgusaldır.

---

## English

Audit area: Active Directory, network devices, VLAN segmentation, password security
Basis: the company's own Information Security Policy and Password Policy

What I was asked to do: compare the IT infrastructure of a 70-person software company in Istanbul against its own written policies, fill in missing information with questions, and report the findings as Gap / Cause / Impact / Recommendation.

Scenario (fictional): one Domain Controller, two physical servers, six switches, two Wi-Fi access points, three VLANs (Admin, Developer, Guest) and a Cisco ASA 5505 firewall. IT staff state that strong passwords are used and the password policy is enforced.

How I did it: I prepared a question list first (Appendix 1). I tested the root password hash taken from the switch's /etc/shadow with Hashcat; it was an unsalted SHA-1 and cracked to "admin123". I then checked Domain Admins membership, the Guest account, Audit Policy and GPO settings, the VLAN design and device versions against the policies.

Result: 6 findings, 3 Critical, 3 High: a cracked switch root password, non-admin users in Domain Admins, an enabled Guest account with no password, audit policy off and no GPO-enforced password policy, unclear VLAN separation, and network devices that no longer receive updates.

The report is written in Turkish. All companies, usernames, passwords and hashes are fictional.

[Portföy ana sayfası / Back to portfolio](../README.md)
