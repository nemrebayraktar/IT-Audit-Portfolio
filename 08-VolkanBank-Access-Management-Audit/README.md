# 08 - VolkanBank: Access Management & Password Security Audit

Çerçeve / Framework: IAM lifecycle, SoD, MFA, password hashing (MD5 vs bcrypt/Argon2), ISO 27001 / PCI-DSS references

[Türkçe](#türkçe) | [English](#english)

## Türkçe

Denetim alanı: Erişim Yönetimi ve Parola Güvenliği Denetimi

### Benden istenen
Kullanıcı listesi, işten ayrılan personel, parola politikası, parola hash dökümü, erişim gözden geçirme prosedürü ve ortak hesap kanıtlarından en az 5 bulgu çıkarmak (risk / etki / öneri); "Parolalarımız güçlüdür" iddiasını değerlendirmek; hash algoritmasını analiz etmek; en kritik bulguyu iş etkisiyle açıklamak ve Yönetim Kurulu için en fazla 5 cümlelik özet yazmak.

### Senaryo (kurgusal)
CIO yetkisiz erişime karşı parola kontrollerinin güçlü ve yeterli olduğunu beyan ediyor.

### Yöntem
Kullanıcı ve işten ayrılan personel listeleri karşılaştırıldı, parola politikası ve prosedür kanıtla test edildi, hash'ler yapısından MD5 olarak tanımlanıp kırılabilirlikleri doğrulandı. Bulgular Risk / Etki / Öneri formatında yazıldı ve en kritik bulgu senaryo ve potansiyel zarar ile analiz edildi.

### Temel bulgular
6 bulgu (raporda seviye derecelendirmesi yok); en kritik bulgu: 14 ay önce ayrılmış personelin Domain Admins ve VPN Users üyesi, parolası süresiz ve zayıf hesabının aktif olması. Diğerleri: opsiyonel karmaşıklık/MFA ve kapalı kilitleme, MD5 ile saklanan ve saniyeler içinde kırılan parolalar, ortak admin/support hesapları, VPN'de MFA yokluğu, 18 aydır ertelenen erişim gözden geçirmesi.

### Kullanılan yetkinlikler
IAM / JML · Password & hash analysis · Business impact translation · Executive summary writing

### Dosyalar
- [VolkanBank-Access-Audit-Report-TR.pdf](VolkanBank-Access-Audit-Report-TR.pdf): Denetim raporu
- [Lab-Brief-and-Evidence-TR.pdf](Lab-Brief-and-Evidence-TR.pdf): Vaka dokümanları ve görevler

Not: Bu çalışmadaki şirket, kişi, hesap, IP ve diğer tüm veriler eğitim için oluşturulmuş kurgusal verilerdir. Rapor Türkçedir.

## English

Audit area: Access Management & Password Security Audit

### What I was asked to do
From the user list, leaver list, password policy, password hash extract, access review procedure and shared account evidence: identify at least 5 findings (risk / impact / recommendation), assess the claim "our passwords are strong", analyse the hash algorithm, explain the most critical finding in business terms and write a board summary of at most 5 sentences.

### Scenario (fictional)
The CIO states that password controls against unauthorised access are strong and sufficient.

### Methodology
User and leaver lists were reconciled, the password policy and procedure were tested against evidence, and hashes were identified as MD5 from their structure and shown to be crackable. Findings use Risk / Impact / Recommendation, and the most critical finding was analysed with an attack scenario and potential damage.

### Key findings
6 findings (no severity scale in the report); most critical: an account of an employee who left 14 months ago is still active, a member of Domain Admins and VPN Users, with a weak non-expiring password. Others: optional complexity/MFA and disabled lockout, MD5-stored passwords cracked within seconds, shared admin/support accounts, no MFA on VPN, an access review postponed for 18 months.

### Skills used
IAM / JML · Password & hash analysis · Business impact translation · Executive summary writing

### Files
- [VolkanBank-Access-Audit-Report-TR.pdf](VolkanBank-Access-Audit-Report-TR.pdf): Audit report
- [Lab-Brief-and-Evidence-TR.pdf](Lab-Brief-and-Evidence-TR.pdf): Case documents and tasks

Note: All companies, people, accounts, IPs and other data in this work are fictional and were created for training. The report is in Turkish.

---
[Ana sayfa / Back to main page](../README.md)
