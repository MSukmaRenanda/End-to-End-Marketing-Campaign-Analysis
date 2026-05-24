# End-to-End-Marketing-Campaign-Analysis
End to End Marketing Campaign Analysis using Microsoft Excel &amp; Power BI
📌 Deskripsi Proyek
Proyek ini menganalisis dataset telemarketing bank Portugal untuk menjawab pertanyaan bisnis utama: siapa pelanggan yang paling mungkin berlangganan term deposit, dan faktor kampanye apa yang mendorong konversi?
Analisis dilakukan secara end-to-end menggunakan Excel untuk validasi statistik dan Power BI untuk visualisasi strategis, mencakup data cleaning, feature engineering, EDA, statistical testing, hingga business recommendation.

❓ Problem Statement

Profil pelanggan mana yang paling mungkin berlangganan term deposit?
Apakah durasi panggilan secara signifikan memengaruhi hasil konversi?
Seberapa besar pengaruh keberhasilan kampanye sebelumnya terhadap perilaku langganan di masa depan?


🎯 Objektif
NoObjektifOutput1Customer SegmentationIdentifikasi kelompok demografis dengan conversion rate tertinggi2Campaign EffectivenessAnalisis intensitas kampanye dan durasi panggilan terhadap konversi3Previous Campaign ImpactUji apakah hasil kampanye sebelumnya memprediksi langganan saat ini4Strategic DashboardDashboard Power BI interaktif untuk monitoring performa kampanye

📂 Dataset
AtributDetailSumberUCI Machine Learning RepositoryKonteksKampanye telemarketing bank PortugalRaw Data41.188 baris · 21 kolomPeriode2008 – 2010TargetKolom y (yes/no) — apakah pelanggan berlangganan
Kelompok Fitur:

Demografis: Age, Job, Marital, Education
Finansial: Balance, Housing, Loan
Kampanye: Contact, Duration, Campaign
Hasil Sebelumnya: Poutcome
Target: Y


🧹 Data Cleaning
LangkahDetailBaris TerdampakMissing Values0 missing values ditemukan—Duplicates0 duplikat ditemukan—Contact UnknownDidrop — conversion rate sangat rendah-8.996 barisEducation UnknownDidrop — di bawah threshold 30%-1.191 barisPoutcome UnknownDipertahankan sebagai "No Previous Contact"81% dataFinal Dataset31.011 baris

⚙️ Feature Engineering
4 kolom baru dibuat untuk analisis yang lebih dalam:
Kolom BaruKategoriTujuanCampaign_IntensityLow (1-2) · Medium (3-5) · High (6+)Identifikasi frekuensi kontak optimalAge_GroupYoung Adult · Adult · Senior Adult · Super SeniorTargeting berbasis profil usiaCustomer_Risk_FlagNormal · Active Loan CustomerStrategi kampanye berbasis risikoBalance_SegmentNegative · Low · Medium · High · PremiumSegmentasi berbasis kekayaan

📊 Hasil Analisis
1. Overall Performance

Total Calls: 31.011
Total Subscriptions: 4.528
Conversion Rate: 14.6%
Baseline ini membuktikan bahwa mass marketing tanpa filter memiliki failure rate 85.4%

2. Customer Profile
DimensiTemuanJobManagement & Retired → conversion rate tertinggi; Blue-collar → terendahEducationTertiary lebih efisien (17.4%) vs Secondary (13.5%), meski Secondary dominan volumeAge GroupSuper Senior (37%) dan Young Adult (22%) melampaui kelompok usia lainnyaMarital StatusMarried dominan volume; Single konversi lebih tinggi secara proporsional
3. Campaign Performance
DimensiTemuanBest Conv. Rate MonthMarch — conversion rate tertinggi per callPeak Volume MonthAugust — jumlah subscriber terbanyakCampaign IntensityLow (1-2 kontak) → 55.23% volume sukses; High (6+) → hanya 0.65%Previous OutcomeSuccess: 64.8% · Failure: 12.5% · No Previous: 11.8%
4. Statistical Testing
T-Test: Durasi Panggilan vs Konversi

Subscribers: rata-rata 506.8 detik
Non-subscribers: rata-rata 218.3 detik
p-value: 0.000 → Signifikan
⚠️ Catatan: durasi adalah konsekuensi konversi, bukan penyebab — tidak boleh digunakan sebagai prediktor

Chi-Square: Hasil Kampanye Sebelumnya vs Konversi

p-value: 0.000 → Signifikan
Pelanggan dengan riwayat sukses memiliki conversion rate 5x lebih tinggi


💡 Rekomendasi Bisnis

Retargeting Past Successes — Prioritaskan pelanggan dengan riwayat sukses kampanye (64.8% conversion rate) di urutan teratas call list harian
Risk-Based Targeting — Fokus pada pelanggan tanpa housing loan di segmen medium balance
Dual Script Strategy — Buat dua pendekatan script berbeda: future-planning untuk Student/Young Adult, dan asset stability untuk Retired/Super Senior
Less is More — Batasi kontak maksimal 1-2x per pelanggan; high-intensity campaign hanya menghasilkan 0.65% conversion
Efficient Segment Targeting — Prioritaskan pelanggan Tertiary educated (17.4% conversion rate) dibanding Secondary (13.5%) untuk hasil yang lebih efisien per call

🛠️ Tools yang Digunakan

Microsoft Excel — Data cleaning, feature engineering, EDA, statistical testing (T-Test, Chi-Square), pivot table, executive summary dashboard
Power BI — Interactive dashboard, DAX measures, customer profile analysis, campaign performance analysis

👤 Author
Muhamad Sukma Renanda

📧 muhamadsukmarenanda@gmail.com
🔗 [LinkedIn](https://www.linkedin.com/in/muhamad-sukma-renanda/)
🌐 [Portfolio](https://muhamadsukmarenanda.wixsite.com/portofolio-da)
