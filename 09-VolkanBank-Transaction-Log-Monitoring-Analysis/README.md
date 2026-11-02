# 09 · VolkanBank — Transaction Log Monitoring & Incident Analysis

`Log Analysis · Monitoring · RCA` · **Framework:** Log correlation, latency/trend analysis, monitoring & alert thresholds, Incident & Change Management, RCA

[🇹🇷 Türkçe](#-türkçe) · [🇬🇧 English](#-english)

---

## 🇹🇷 Türkçe

**Denetim alanı:** İşlem Logu İzleme ve Olay Analizi

### Benden istenen
İnternet bankacılığında "transferler bazen başarısız oluyor, sistem donuyor" şikayetlerine karşın monitoring alarm üretmemektedir. Ödeme sistemi loglarını inceleyerek anormalliği kanıtlamak, kök nedeni, alarm üretilmeme sebebini ve iş etkisini (müşteri, operasyonel, finansal, itibar) açıklamak, öneri sunmak ve 5 cümlelik Yönetim Kurulu özeti yazmak.

### Senaryo (kurgusal)
BT Operasyon ekibi monitoring sistemlerinde kritik alarm görünmediğini belirtiyor; iç denetim log incelemesi talep ediyor.

### Yöntem
24.000 satırlık uygulama logunda zaman damgası aralıkları, gecikme (latency) değerleri ve HTTP hata kodları korelasyonu yapıldı; normal 10 ms ritmindeki boşluklar ve ardından gelen hatalar tespit edildi.

### Temel bulgular
**Ana bulgu:** 09:00:13.753Z–09:00:13.851Z arasında ~98 ms tüm servislerde log sessizliği ve hemen ardından `PUT /api/v1/payments` işleminde 502 `upstream_timeout` (latency 99 ms); ayrıca dağınık 500/502 hataları. Kök neden: senkron upstream bağımlılığı (ödeme geçidi / ortak veritabanı). Alarm yok çünkü izleme 1–5 dakikalık ortalamalara bakıyor. Öneriler: Circuit Breaker, asenkron kuyruk mimarisi, P95/P99 ve 5xx oranı eşikleri, APM.

### Gösterilen yetkinlikler
Log analysis · Monitoring design · Root Cause Analysis · Business impact analysis

### Dosyalar
- [`VolkanBank-Log-Monitoring-Report-TR.pdf`](VolkanBank-Log-Monitoring-Report-TR.pdf) — Analiz raporu
- [`Lab-Brief-TR.pdf`](Lab-Brief-TR.pdf) — Vaka senaryosu ve sorular
- [`evidence/transaction_log_analysis_lab.log`](evidence/transaction_log_analysis_lab.log) — Analiz edilen uygulama logu (eğitim verisi)

> ⚠️ Bu çalışmadaki şirket, kişi, kullanıcı, IP ve tüm veriler eğitim amaçlı oluşturulmuş **kurgusal** verilerdir; gerçek bir kurumu temsil etmez. Rapor dili Türkçedir.

---

## 🇬🇧 English

**Audit area:** Transaction Log Monitoring & Incident Analysis

### What I was asked to do
Customers report failed transfers and brief freezes in internet banking, yet monitoring shows no alerts. Analyse payment-system logs to prove the anomaly, explain the root cause, why no alert fired and the business impact (customer, operational, financial, reputational), recommend fixes and write a 5-sentence board summary.

### Scenario (fictional)
IT Operations says monitoring shows no critical alarms; internal audit requests a log review.

### Methodology
Timestamp gaps, latency values and HTTP error codes were correlated across a 24,000-line application log, revealing breaks in the normal ~10 ms cadence followed by errors.

### Key findings
**Key finding:** a ~98 ms platform-wide log silence between 09:00:13.753Z and 09:00:13.851Z, immediately followed by a 502 `upstream_timeout` on `PUT /api/v1/payments` (latency 99 ms), plus scattered 500/502 errors. Root cause: a synchronous upstream dependency (payment gateway / shared database). No alert because monitoring uses 1–5 minute averages. Recommendations: circuit breaker, asynchronous queuing, P95/P99 and 5xx-rate thresholds, APM.

### Skills demonstrated
Log analysis · Monitoring design · Root Cause Analysis · Business impact analysis

### Files
- [`VolkanBank-Log-Monitoring-Report-TR.pdf`](VolkanBank-Log-Monitoring-Report-TR.pdf) — Analysis report
- [`Lab-Brief-TR.pdf`](Lab-Brief-TR.pdf) — Case brief and questions
- [`evidence/transaction_log_analysis_lab.log`](evidence/transaction_log_analysis_lab.log) — Application log analysed (training data)

> ⚠️ All companies, people, accounts, IPs and data in this work are **fictional** and created for training; they do not represent any real organisation. The report is written in Turkish.

---
[⬅ Portföy ana sayfası / Back to portfolio](../README.md)
