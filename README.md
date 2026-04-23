# Analisis Potensi Investasi Deposito Nasabah 🏦📊

Proyek *Exploratory Data Analysis* (EDA) ini bertujuan untuk mengidentifikasi nasabah *existing* yang memiliki potensi tertinggi untuk berinvestasi pada produk simpanan jangka panjang (deposito). Analisis ini dilakukan untuk mendukung strategi bisnis bank dalam meningkatkan *Customer Lifetime Value* (CLV).

## 🎯 Objektif Proyek
1. Melakukan eksplorasi data untuk melihat hubungan antara profil nasabah dan keputusan berlangganan deposito (`subscription`).
2. Menganalisis pola perilaku nasabah berdasarkan usia, saldo bulanan rata-rata, dan status pinjaman.
3. Merumuskan tipe nasabah (segmentasi) yang paling potensial untuk ditargetkan oleh *Relationship Manager* (RM).

## 📂 Informasi Dataset
Dataset yang digunakan berisi 30 baris data nasabah dengan 15 kolom atribut. Data terindikasi bersih tanpa adanya *missing values* (0 total *missing*).

**Fitur Utama:**
* **Demografi:** `age`, `job`, `marital`, `education`.
* **Finansial & Produk:** `avg_monthly_balance`, `total_products_owned`, `years_as_customer`.
* **Pinjaman & Investasi:** `housing_loan`, `personal_loan`, `credit_card`, `investment_experience`.
* **Interaksi Bisnis:** `contact_channel`, `relationship_manager_contact`.
* **Target Variabel:** `subscription` (yes/no).

## 🛠️ Alat & Teknologi (Tech Stack)
Proyek ini dikembangkan menggunakan Python dengan beberapa pustaka utama untuk manipulasi dan visualisasi data:
* `pandas` 
* `numpy` 
* `matplotlib` 
* `seaborn` 

## 💡 Temuan Utama (Key Insights)
Berdasarkan analisis yang telah dilakukan, nasabah yang berlangganan (Subscriber) memiliki perbedaan profil yang sangat kontras dibandingkan dengan yang tidak berlangganan (Non-Subscriber):
* **Faktor Usia & Saldo:** *Subscriber* umumnya adalah nasabah senior dengan usia rata-rata 50.5 tahun (batas bawah ~40 tahun) dan memiliki saldo rata-rata Rp 24.5 Juta (5.3x lebih tinggi dari *non-subscriber*).
* **Loyalitas:** *Subscriber* memiliki *engagement* yang jauh lebih tinggi, rata-rata sudah menjadi nasabah selama 15.3 tahun dan memiliki 4.2 produk bank.
* **Hambatan Utama (Barrier):** Kepemilikan cicilan rumah/KPR (*housing loan*) sangat menurunkan rasio *subscription* hingga hanya 11.4%. Sebaliknya, nasabah tanpa KPR memiliki *success rate* sebesar 66.7%.
* **Faktor Penentu Mutlak (Perfect Predictors):** Variabel `investment_experience` (pengalaman investasi) dan `relationship_manager_contact` (kontak dari RM) memisahkan target secara sempurna dengan akurasi 100%.

## 🎯 Profil Target Ideal
Nasabah paling potensial untuk ditargetkan oleh *Relationship Manager* memiliki karakteristik berikut:
* Usia $\ge$ 41 tahun.
* Saldo bulanan rata-rata $\ge$ Rp 15 juta.
* Lama menjadi nasabah $\ge$ 9 tahun.
* Memiliki $\ge$ 3 produk bank.
* Tidak memiliki *housing loan* aktif.
* Pekerjaan: *management*, *retired*, *self-employed*, atau *entrepreneur*.
* Pendidikan: *tertiary* atau *primary (senior)*.

## 🚀 Rekomendasi Bisnis
1. **Prioritaskan Kontak Personal:** RM harus lebih proaktif menghubungi nasabah secara personal, mengingat variabel ini memiliki korelasi 100% terhadap konversi.
2. **Edukasi Investasi Dasar:** Gunakan program literasi keuangan sebagai langkah awal untuk membangun `investment_experience` sebelum menawarkan produk deposito *.
3. **Fokus Segmen High-Value:** Optimalkan sumber daya pada nasabah berusia $\ge$ 40 tahun dengan saldo $\ge$ Rp 15 Juta.
4. **Efisiensi Targeting:** Hindari penawaran investasi jangka panjang pada nasabah dengan beban *housing loan* aktif.

---
*Dibuat berdasarkan Pre-Challenge 2b - Data Science Track* [cite: 1]
