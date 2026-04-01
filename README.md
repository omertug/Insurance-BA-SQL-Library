TR | Sigorta Çekirdek Sistem Veri Modeli ve Analitik Sorgular
Proje Hakkında:
Bu proje, modern bir sigorta ana yazılımının (Core System) kalbinde yer alan veri mimarisini modellemektedir. Bir İş Analisti gözüyle; poliçe yaşam döngüsü, müşteri yönetimi, hasar süreçleri ve zeyl (endorsement) operasyonlarını kapsayan kapsamlı bir PostgreSQL şeması sunar.

Özellikler:
Standardize İsimlendirme: D_, P_, L_, T_ ön ekleriyle kurumsal standartlarda tablo yapısı.
Business Intelligence (BI) Odaklılık: Üretim, Hasar ve Bölge Müdürlükleri için kritik KPI sorguları.
Uçtan Uca Süreç: Teklif aşamasından hasar ödemesine kadar tüm entegrasyon noktaları.

Ön Ek,Açıklama,Örnek Tablo (Sigortacılık)
D_ (Data/Master),Sistemin ana nesneleri.,"D_CUSTOMER, D_POLICY, D_AGENCY"
P_ (Parameter),Sabit veya nadir değişen tanımlar.,"P_CITY, P_PRODUCT_TYPE, P_CURRENCY"
L_ (Log/Audit),Geçmiş izleri ve sistem logları.,"L_LOGIN_ATTEMPTS, L_TABLE_AUDIT"
T_ (Transaction),Sürekli akan mali veya operasyonel hareketler.,"T_COLLECTION (Tahsilat), T_PAYMENT"
H_ (History),Verinin eski versiyonlarını tutan tablolar.,H_POLICY_VERSION (Zeyl sonrası eski poliçeler)
S_ (Summary),Raporlama için önceden hesaplanmış özet veriler.,"S_MONTHLY_PRODUCTION, S_AGENCY_KPI"
B_ (Bridge),Çoktan çoğa (M2M) ilişkileri bağlayan tablolar.,B_POLICY_COVERAGE (Poliçe ve Teminat eşleşmesi)

EN | Insurance Core System Data Model & Analytical Queries
Project Overview:
This repository showcases a robust PostgreSQL data architecture designed for a modern Insurance Core System. Developed from a Business Analyst's perspective, the project covers the entire policy lifecycle, including customer management, claims processing, and endorsement (endorsement) operations.

Key Highlights:

Standardized Naming Convention: Utilizes enterprise-level prefixes (D_ for Data, P_ for Parameters, L_ for Logs, T_ for Transactions).
Business Insights: Includes complex SQL queries tailored for Production, Claims, and Regional Management departments to track critical KPIs.
Domain Expertise: Reflects real-world insurance business logic, from premium calculations to loss ratio analysis.

