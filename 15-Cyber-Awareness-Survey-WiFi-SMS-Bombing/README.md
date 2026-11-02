# 15 - Bireysel Siber Güvenlik Farkındalık Anketi: Wi-Fi ve SMS Bombing

Türkçe | [English](#english)

Konu: Kullanıcıların Wi-Fi saldırıları, SMS bombing ve e-posta veri sızıntıları konusundaki farkındalığı

## Ne yaptım

Kendi başlattığım bağımsız bir çalışma. İki bölümden oluşuyor:

1. Wi-Fi (10.10.2025): Yaklaşık 60-80 kişiye deauth ve Evil Twin gibi saldırıları bilip bilmediklerini sordum. Yaklaşık 10 kafede ve çok sayıda yurt odasında kullanılan Wi-Fi türünü ve sistem yeterliliğini (şifreleme, şifre değişikliği, 2.4 GHz kullanımı, giriş sayfalarında HTTP / HTTPS) sorarak ve gözlemleyerek değerlendirdim. Hiçbir ağa saldırı ya da müdahale yapılmadı.
2. SMS bombing ve e-posta sızıntıları (12.11.2025): Yakın çevremden 40 kişinin anonimleştirilmiş verisiyle e-posta sızıntılarını Have I Been Pwned üzerinden kontrol ettim, SMS bombing vakalarını mağdurlardan dinledim.

Hiçbir kişisel veri, ağ adı veya cihaz bilgisi kaydedilmedi; sonuçlar yalnızca oran olarak verildi.

## Sonuçlar

- Kullanıcıların %60'ı deauth saldırısının bağlantıyı kesebileceğini bilmiyor, bunların %80'i bunun Evil Twin saldırısının ön adımı olabileceğini bilmiyor.
- Ağların yaklaşık %70'inde Wi-Fi şifresi hiç değiştirilmemiş; incelenen yurtların tamamı 2.4 GHz kullanıyor, yurtlardaki açık ağlarda giriş sayfalarının HTTP üzerinden çalıştığı görüldü.
- 40 kişinin e-posta hesaplarının %80'i en az bir veri ihlalinde yer almış, en eski hesaplardan birinde 16 sızıntı var.
- Kişilerin yaklaşık %50'si kritik hesaplarında bile MFA kullanmıyor.
- Yönlendirmelerden sonra bazı katılımcılar MFA'yı açtı ve zayıf parolalarını değiştirdi.

## Dosyalar

- [Awareness-Survey-Report-TR.pdf](Awareness-Survey-Report-TR.pdf) - İki bölümün birleştirilmiş anket raporu (Türkçe)

---

## English

Topic: user awareness of Wi-Fi attacks, SMS bombing and email data breaches. An independent study I ran myself, in two parts:

1. Wi-Fi (10 Oct 2025): I asked roughly 60-80 people whether they knew about attacks such as deauth and Evil Twin, and asked about the Wi-Fi type and setup (encryption, password changes, 2.4 GHz use, HTTP vs HTTPS login pages) in about 10 cafés and many dorm rooms. No network was attacked or interfered with.
2. SMS bombing and email breaches (12 Nov 2025): using anonymised data from 40 people around me, I checked email breaches on Have I Been Pwned and collected SMS bombing cases from the people affected.

No personal data, network names or device identifiers were recorded; results are reported as percentages only.

Results: 60% of users did not know a deauth attack can drop their connection, and 80% of those did not know it can lead to an Evil Twin attack. About 70% of networks never had their Wi-Fi password changed; all dorms used 2.4 GHz, and HTTP login pages were seen on open dorm networks. 80% of the 40 people's email accounts appeared in at least one breach (one older account in 16), and about 50% did not use MFA even on critical accounts. After guidance, some participants enabled MFA and changed weak passwords.

The reports are written in Turkish.

[Portföy ana sayfası / Back to portfolio](../README.md)
