# 10 · VolkanBank — Authentication Log & Incident Analysis

`Log Analysis · Incident Response · MFA` · **Framework:** Log analysis, MFA attack patterns (MFA fatigue, session hijacking), incident response

[🇹🇷 Türkçe](#-türkçe) · [🇬🇧 English](#-english)

---

## 🇹🇷 Türkçe

**Denetim alanı:** Kimlik Doğrulama Logu ve Olay Analizi

### Benden istenen
Kimlik doğrulama servisine ait log kayıtlarını inceleyerek anormallikleri tespit etmek ve olayı yorumlamak. (Bu çalışmanın ayrı bir senaryo dokümanı dosyalarda bulunmuyor; kapsam rapor ve log dosyasından aktarılmıştır.)

### Senaryo (kurgusal)
20.000 satırlık log kaydında, 18 Haziran 2026 gecesi yalnızca `admin` hesabına ait giriş işlemleri yer alıyor.

### Yöntem
Log alanları (status, ip, mfa, session_id, user_agent, zaman damgası) örüntü açısından analiz edildi ve davranış insan kullanımıyla karşılaştırıldı.

### Temel bulgular
**5 anormallik** ve sonuç: admin hesabı dağıtık bir ağ (botnet/proxy) üzerinden ele geçirilmiş, MFA aşılmış. Kanıtlar: saniyeler içinde ardışık başarılı girişler, tüm girişlerde `mfa=passed`, her girişte farklı IP, sürekli değişen User-Agent, ~2 saatte yüzlerce yeni oturum. Olası yöntemler: MFA Fatigue, MFA anahtarı hırsızlığı, Session Token Manipulation. Öneri: hesabın kapatılması, tüm oturumların sonlandırılması, kimlik doğrulama altyapısının incelenmesi.

### Gösterilen yetkinlikler
Log analysis · Threat detection · Incident response · MFA attack awareness

### Dosyalar
- [`VolkanBank-Auth-Log-Analysis-Report-TR.pdf`](VolkanBank-Auth-Log-Analysis-Report-TR.pdf) — Analiz raporu
- [`evidence/authentication_logs.log`](evidence/authentication_logs.log) — Analiz edilen kimlik doğrulama logu (eğitim verisi)

> ⚠️ Bu çalışmadaki şirket, kişi, kullanıcı, IP ve tüm veriler eğitim amaçlı oluşturulmuş **kurgusal** verilerdir; gerçek bir kurumu temsil etmez. Rapor dili Türkçedir.

---

## 🇬🇧 English

**Audit area:** Authentication Log & Incident Analysis

### What I was asked to do
Review authentication-service logs, identify anomalies and interpret the incident. (No separate brief exists for this exercise; scope is taken from the report and the log file.)

### Scenario (fictional)
A 20,000-line log in which every entry is an `admin` login during the night of 18 June 2026.

### Methodology
Log fields (status, ip, mfa, session_id, user_agent, timestamp) were analysed for patterns and compared with plausible human behaviour.

### Key findings
**5 anomalies** and a conclusion: the admin account was compromised via a distributed network (botnet/proxy) and MFA was bypassed. Evidence: back-to-back successful logins within seconds, `mfa=passed` on every login, a different IP each time, rotating User-Agents, hundreds of new sessions in ~2 hours. Likely vectors: MFA fatigue, stolen MFA seed, session token manipulation. Recommendation: disable the account, kill all sessions, investigate the authentication stack.

### Skills demonstrated
Log analysis · Threat detection · Incident response · MFA attack awareness

### Files
- [`VolkanBank-Auth-Log-Analysis-Report-TR.pdf`](VolkanBank-Auth-Log-Analysis-Report-TR.pdf) — Analysis report
- [`evidence/authentication_logs.log`](evidence/authentication_logs.log) — Authentication log analysed (training data)

> ⚠️ All companies, people, accounts, IPs and data in this work are **fictional** and created for training; they do not represent any real organisation. The report is written in Turkish.

---
[⬅ Portföy ana sayfası / Back to portfolio](../README.md)
