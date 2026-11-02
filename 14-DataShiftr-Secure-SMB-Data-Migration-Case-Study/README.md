# 14 - DataShiftr: İnternet Üzerinden Güvenli Veri Taşıma (Vaka Analizi)

Türkçe | [English](#english)

Konu: Windows Server 2012 R2'den Windows Server 2019'a SMB 3 şifrelemesiyle veritabanı aktarımı

## Benden istenen

Farklı ülkelerdeki iki sunucu arasında, kanuni bir zorunluluk nedeniyle büyük bir veritabanını güvenli ve maliyet etkin şekilde taşımak. Kurallar: sunucular güncellenemez, sadece SMB kullanılabilir, ağlar birleştirilemez, VPN açılamaz, veri yalnızca internet üzerinden gidebilir ve hiçbir üçüncü tarafa (bulut depolama dahil) uğramamalıdır.

## Nasıl çözdüm

USB ile kargolama, bulut depolama ve VPN seçeneklerini kurallara göre eledim. Windows Server 2019'dan 2012 R2'deki paylaşımı SMB (445) ile map etme yöntemini seçtim. İki sunucu arasında anlaşılan sürüm SMB 3.0.2 olduğu için 2012 R2 tarafında SMB şifrelemesi açıldığında veri AES-128-CCM ile şifreli gider. Bu yöntem ücretsiz ve kurallara uygun. 445 portunu internete açmanın riskini de ayrıca değerlendirdim: portun yalnızca karşı sunucunun IP'sine ve aktarım süresince açılması, şifresiz bağlantıların reddedilmesi, SMBv1'in kapatılması, en az yetkili bir hesap kullanılması ve aktarım öncesi / sonrası hash karşılaştırması.

## Dosyalar

- [DataShiftr-Case-Study-TR.pdf](DataShiftr-Case-Study-TR.pdf) - Vaka analizi (Türkçe)
- [evidence/network-topology.png](evidence/network-topology.png) - Senaryo topolojisi

---

## English

Topic: migrating a database from Windows Server 2012 R2 to Windows Server 2019 over the internet using SMB 3 encryption.

What I was asked to do: move a large database between two servers in different countries, securely and cheaply, because of a legal requirement. Rules: no server updates, SMB only, networks cannot be merged, no VPN, internet only, and no third party (including cloud storage) may touch the data.

How I solved it: I ruled out shipping USB drives, cloud storage and VPN under the rules, and chose mapping the 2012 R2 share from the 2019 server over SMB (445). The negotiated dialect between the two is SMB 3.0.2, so enabling SMB encryption on the 2012 R2 side encrypts the transfer with AES-128-CCM, at no cost. I also addressed the risk of exposing port 445: allow only the other server's IP and only during the transfer, reject unencrypted access, disable SMBv1, use a least-privilege account, and compare file hashes before and after.

The case study is written in Turkish.

[Portföy ana sayfası / Back to portfolio](../README.md)
