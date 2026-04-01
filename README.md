# 🛡️ Insurance Core System: Data Architecture & SQL Insights
### 🇹🇷 Sigorta Çekirdek Sistem Veri Modeli ve İş Analitiği Sorguları

---

## 📝 Project Overview / Proje Hakkında
**EN:** This project models the data architecture of a modern insurance core system on PostgreSQL. From a business analyst's perspective, it presents a simple, end-to-end structure encompassing production, claims, and endorsement processes.

**TR:** Bu proje, modern bir sigorta ana yazılımının (Core System) PostgreSQL üzerindeki veri mimarisini modellemektedir. Bir **İş Analisti** gözüyle; üretim, hasar ve zeyl süreçlerini kapsayan uçtan uca basit bir yapı sunar.

---

## 🏗️ Database Architecture / Veri Mimarisi
I have used a standardized naming convention to ensure scalability and clarity:
* **`D_` (Data):** Master tables (e.g., `D_POLICY`, `D_CUSTOMER`)
* **`P_` (Parameter):** Static definitions (e.g., `P_PRODUCT_TYPE`, `P_CITY`)
* **`L_` (Log):** System and audit logs (e.g., `L_CLAIM_HISTORY`)
* **`T_` (Transaction):** Financial movements (e.g., `T_COLLECTION`)
* **`H_` (History):** Older versions of data (e.g., `H_POLICY_VERSION`)
* **`S_` (Summary):** Pre-calculated summary data for reporting (e.g., `S_MONTHLY_PRODUCTION`)
* **`B_` (Bridge):** Connecting many-to-many (M2M) relationships (e.g., `B_POLICY_COVERAGE`)

---

## 📊 Business Intelligence & Analytical Queries (KPIs) 
### 🇹🇷 İş Analitiği ve Temel Performans Göstergeleri (KPI)

> **EN:** Below is a list of the business-critical SQL metrics included in this project, designed to provide actionable insights for various insurance departments.

> **TR:** Proje kapsamında yer alan ve sigorta birimleri için kritik veriler sağlayan iş zekası metriklerinin listesi aşağıdadır.

---

### 🏭 Production Management / Üretim Müdürlüğü
* **Monthly GWP Trend / Aylık Brüt Prim Üretimi:**
    * *EN:* Total written premiums and growth analysis by month. 
    * *TR:* Aylık toplam prim üretimi ve büyüme analizi.
* **Product Performance Analysis / Ürün Performans Analizi:**
    * *EN:* Distribution of policy counts and premiums across different branches (Motor, Health, Fire). 
    * *TR:* Branş bazında (Kasko, Sağlık, Yangın) poliçe adedi ve prim dağılımı.
* **Renewal Ratio / Yenileme Oranı:**
    * *EN:* Tracking the percentage of expired policies that were successfully renewed. 
    * *TR:* Vadesi biten poliçelerin yenilenme başarısının takibi.
* **New Business vs. Endorsement Impact / Yeni İş ve Zeyl Etkisi:**
    * *EN:* Analyzing premium changes originating from new sales versus policy amendments. 
    * *TR:* Yeni satışlardan ve zeyl (değişiklik) işlemlerinden gelen prim etkisinin ayrıştırılması.

### 📉 Claims Department / Hasar Müdürlüğü
* **Loss Ratio by Branch / Branş Bazlı Hasar-Prim Oranı:**
    * *EN:* The ultimate KPI for insurance profitability: (Paid + Reserved) / Premium. 
    * *TR:* Sigortacılık karlılığının ana ölçütü: (Ödenen + Muallak) / Prim oranı.
* **Claim Settlement Duration / Hasar Dosya Kapatma Süresi:**
    * *EN:* Average days elapsed from claim notification to final payment. 
    * *TR:* Hasar ihbarı ile dosya ödemesi arasında geçen ortalama gün süresi.
* **Outstanding Reserves (Muallak) / Muallak Hasar Takibi:**
    * *EN:* Monitoring total estimated liability for open claim files (`L_CLAIM_HISTORY`). 
    * *TR:* Açık hasar dosyaları için ayrılan toplam karşılık tutarının takibi.
* **Claim Frequency Analysis / Hasar Frekansı:**
    * *EN:* Identifying regions or product types with the highest incidence of claims. 
    * *TR:* En sık hasar gerçekleşen bölgelerin veya ürünlerin tespiti.

### 📍 Regional & Agency Management / Bölge ve Acente Yönetimi
* **Regional Sales Rankings / Bölge Satış Performansı:**
    * *EN:* Ranking geographical regions based on GWP and policy count. 
    * *TR:* Coğrafi bölgelerin üretim hacmi ve adetlerine göre sıralanması.
* **Agency Churn Analysis / Acente Kayıp Analizi:**
    * *EN:* Identifying agencies that haven't produced a policy in the last 90 days. 
    * *TR:* Son 90 gündür üretim yapmayan inaktif acentelerin tespiti.
* **Agent Commission Reports / Acente Komisyon Raporları:**
    * *EN:* Calculating monthly earnings based on standard product commission rates (`P_PRODUCT`). 
    * *TR:* Ürün bazlı komisyon oranları üzerinden aylık hak ediş hesaplamaları.

### 💰 Finance & Accounting / Finans ve Muhasebe
* **Collection Ratio / Tahsilat Oranı:**
    * *EN:* Comparing written premiums against successfully collected cash flows (`T_TRANSACTION`). 
    * *TR:* Üretilen primlerin tahsilat başarısının nakit akış tabloları ile karşılaştırılması.
* **Overdue Premium Report / Vadesi Geçmiş Primler:**
    * *EN:* Tracking policies with unpaid installments for legal or cancellation actions. 
    * *TR:* İptal veya yasal takip süreci için ödenmemiş taksitlerin takibi.
* **Tax & Fund Reporting / Vergi ve Fon Raporlaması:**
    * *EN:* Calculation of mandatory taxes (BSMV) and legal funds per policy. 
    * *TR:* Poliçe bazlı BSMV ve diğer yasal kesintilerin hesaplanması.
---

## 🛠️ Tech Stack / Kullanılan Teknolojiler
* **Database:** PostgreSQL 15
* **Modeling:** Relational Database Design (ERD)
* **Domain:** Insurance

---

## 📫 Contact / İletişim
**Name:** Ömer ERTUĞ
**Role:** Senior Insurance Business Analyst
**LinkedIn:** (https://www.linkedin.com/in/omerertug/)
